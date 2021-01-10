# Awesome distributed transactions
A curated selection of distributed transactions protocols

## Highly Available Transactions

### Transactional Causal Consistency

[Cure: Strong semantics meets high availability and low latency](https://hal.inria.fr/hal-01270776/document)

[Stronger Semantics for Low-Latency Geo-Replicated Storage](https://www.usenix.org/conference/nsdi13/technical-sessions/presentation/lloyd) (aka Eiger)

[Don’t Settle for Eventual: Scalable Causal Consistency for Wide-Area Storage with COPS](https://www.cs.cornell.edu/courses/cs6452/2012sp/papers/cops-sosp11.pdf)

### Slightly better than read committed (MAV & RA)

MAV provides "cut isolation" and atomicity. RA is MAV which prevents fractured reads.

[Highly Available Transactions: Virtues and Limitations](https://www.vldb.org/pvldb/vol7/p181-bailis.pdf)

[Scalable Atomic Visibility with RAMP Transactions](http://people.eecs.berkeley.edu/~alig/papers/ramp.pdf)

## Slightly weaker than snapshot isolation levels (PSI, PC-PSI, NMSI)

Compared to snapshot isolation (SI) PSI, PC-PSI & NMSI allows "long fork" anomaly.

[Database Replication Using Generalized Snapshot Isolation](https://infoscience.epfl.ch/record/53561/files/srds2005-gsi.pdf)

[Transactional storage for geo-replicated systems](http://www.news.cs.nyu.edu/~jinyang/pub/walter-sosp11.pdf) (aka Walter, PSI)

[I Can’t Believe It’s Not Causal! Scalable Causal Consistency with No Slowdown Cascades](https://www.usenix.org/conference/nsdi17/technical-sessions/presentation/mehdi) (aka Occult, PC-PSI)

[Non-Monotonic Snapshot Isolation](https://hal.inria.fr/hal-00643430v4/document) (aka Jessy, NMSI)

## Snapshot isolation

[Large-scale Incremental Processing Using Distributed Transactions and Notifications](https://research.google/pubs/pub36726/) (aka Percolator)

## Serializability

[Notes on Data Base Operating Systems](https://link.springer.com/chapter/10.1007%2F3-540-08755-9_9) (aka 2PC, two-phase commit, it all started there)

Let's put 2PC coordinator on Paxos:

  * [Reducing the Cost for Non-Blocking in Atomic Commitment](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.29.6196&rank=1) (aka MD3PC)
  * [Increasing the Resilience of Distributed and Replicated Database Systems](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.3204&rank=1) (aka E3PC)
  * [Consensus on Transaction Commit](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.159.6749&rank=1) (aka paxos commit)

Concurency control schemes:

  * [Extracting More Concurrency from Distributed Transactions](https://www.usenix.org/system/files/conference/osdi14/osdi14-paper-mu.pdf) (aka RoCoCo)
  * [An Evaluation of Distributed Concurrency Control](https://www.vldb.org/pvldb/vol10/p553-harding.pdf)
  * [Strong consistency is not hard to get: Two-Phase Locking and Two-Phase Commit on Thousands of Cores](https://www.vldb.org/pvldb/vol12/p2325-barthels.pdf)

[CockroachDB: The Resilient Geo-Distributed SQL Database](https://dl.acm.org/doi/pdf/10.1145/3318464.3386134) (aka Parallel Commits)

[Calvin: Fast Distributed Transactions for Partitioned Database Systems](http://cs.yale.edu/homes/thomson/publications/calvin-sigmod12.pdf)

[Ocean Vista: Gossip-Based Visibility Control for Speedy Geo-Distributed Transactions](http://www.vldb.org/pvldb/vol12/p1471-fan.pdf)

[Building Consistent Transactions with Inconsistent Replication](https://irenezhang.net/papers/tapir-sosp15.pdf) (aka TAPIR)

[SLOG: Serializable, Low-latency, Geo-replicated Transactions](http://www.vldb.org/pvldb/vol12/p1747-ren.pdf)

Independent transactions (aka one-shot transactions):

  * [Granola: Low-Overhead Distributed Transaction Coordination](https://www.usenix.org/system/files/conference/atc12/atc12-final118.pdf)
  * [Consolidating Concurrency Control and Consensus for Commits under Conflicts](https://www.usenix.org/system/files/conference/osdi16/osdi16-mu.pdf) (aka Janus, "Granola meets TAPIR")

## Special hardware

[The End of a Myth: Distributed Transactions Can Scale](http://www.vldb.org/pvldb/vol10/p685-zamanian.pdf/) (aka NAM-DB, SI)

[No compromises: distributed transactions with consistency, availability, and performance](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/SOSP15-final227.pdf) (aka FaRM, serializability)

[FaSST: Fast, Scalable and Simple Distributed Transactions with Two-Sided (RDMA) Datagram RPCs](https://www.usenix.org/system/files/conference/osdi16/osdi16-kalia.pdf)

## Limits of distributed transactions

[The SNOW Theorem and Latency-Optimal Read-Only Transactions](https://www.usenix.org/system/files/conference/osdi16/osdi16-lu.pdf)
    
[Causal Consistency and Latency Optimality: Friend or Foe?](https://arxiv.org/abs/1803.04237)

[Distributed Transactional Systems Cannot Be Fast](https://arxiv.org/abs/1903.09106)

[Distributed transactional reads: the strong, the quick, the fresh and the impossible](https://arxiv.org/abs/1810.01698)
