✅ 10-Day LLD Practice Plan

| Day        | Problem                                     | Core Concepts & Patterns                                  |
| ---------- | ------------------------------------------- | --------------------------------------------------------- |
| **Day 1**  | 🛡️ In-Memory Rate Limiter (Token Bucket)   | Concurrency, thread-safe design, Strategy, Decorator      |
| **Day 2**  | 🔐 Distributed Lock Manager (Redlock-style) | Quorum, failover, consistency, Singleton, Rollback        |
| **Day 3**  | 🔗 URL Shortener                            | Unique ID generation, Base62 encoding, Repository pattern |
| **Day 4**  | ⚖️ Consistent Hashing / Load Balancer       | Ring-based hashing, Sharding, Strategy, LRU               |
| **Day 5**  | ⏰ Task Scheduler (Retry + Delay)            | Delay queue, exponential backoff, retry policy, Command   |
| **Day 6**  | 📣 Notification Service                     | Observer pattern, async fan-out, event queue              |
| **Day 7**  | 🏢 Elevator System                          | State, Strategy, Command, Scheduling logic                |
| **Day 8**  | 🍽️ Food Delivery System                    | Geo matching, order pipeline, Strategy, Builder, Facade   |
| **Day 9**  | 📱 Social Media Feed Generator              | Feed ranking, Fan-out vs pull, Observer, Template Method  |
| **Day 10** | 📨 Kafka-like Message Queue                 | Topic-based pub-sub, offset mgmt, thread safety, Batching |


🧠 Bonus Add-ons (if time permits)
| Topic                    | Reason                                           |
| ------------------------ | ------------------------------------------------ |
| LRU / LFU Cache          | Eviction strategies, Map + LinkedList, Decorator |
| File Storage (HDFS-lite) | Chunking, Replication, Fault Tolerance           |
| Re-entrant Locks         | Multithreading + fairness                        |
| Cron Parser              | Expression parsing, scheduling logic             |
| Distributed Counter      | Atomicity across nodes                           |

📌 Design Pattern Coverage Summary
| Pattern         | Applied In                                 |
| --------------- | ------------------------------------------ |
| Strategy        | Rate Limiter, Food Delivery, Elevator      |
| Observer        | Notification, Social Feed                  |
| State           | Elevator                                   |
| Command         | Elevator, Scheduler                        |
| Singleton       | Lock Manager                               |
| Template Method | Feed Generator                             |
| Builder         | Food Delivery                              |
| Decorator       | Rate Limiter                               |
| Factory         | Food Delivery (vehicle strategy, matching) |
