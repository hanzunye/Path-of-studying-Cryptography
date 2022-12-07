# Learn “Handbook of applied cryptography”

# Chapter 1: Overview

### 1.1 Information security objectives:

| privacy or confidentiality | keeping information secret from all but those who are authorized to see it. |
| --- | --- |
| data integrity | ensuring information has not been altered by unauthorized or unknown means. |
| entity authentication or identification | corroboration of the identity of an entity (e.g., a person, a computer terminal, a credit card, etc.). |
| message authentication | corroborating the source of information; also known as data origin authentication. |
| signature | a means to bind information to an entity. |
| authorization | conveyance, to another entity, of official sanction to do or be something. |
| validation | a means to provide timeliness of authorization to use or manipulate information or resources. |
| access control | restricting access to resources to privileged entities. |
| certification | endorsement of information by a trusted entity. |
| timestamping | recording the time of creation or existence of information. |
| witnessing | verifying the creation or existence of information by an entity other than the creator. |
| receipt | acknowledgement that information has been received. |
| confirmation | acknowledgement that services have been provided. |
| ownership | a means to provide an entity with the legal right to use or transfer a resource to others. |
| anonymity | concealing the identity of an entity involved in some process. |
| non-repudiation | preventing the denial of previous commitments or actions. |
| revocation | retraction of certification or authorization. |

### 1.2 Cryptographic goals:

Confidentiality, Data integrity, Authentication, Non-repudiation

### 1.3 A taxonomy of cryptographic primitives

![Untitled](Learn%20%E2%80%9CHandbook%20of%20applied%20cryptography%E2%80%9D%2057e2d737a5304618bd85976a47c19406/Untitled.png)

### 1.4 Background of functions

**One-way function:** A function f from a set X to a set Y is called a one-way function if f(x) is “easy” to compute for all x ∈ X but for “essentially all” elements y ∈ Im(f) it is “computationally infeasible” to find any x ∈ X such that f(x) = y.

**Example:** A prime number is a positive integer greater than 1 whose only positive integer divisors are 1 and itself. Select primes p = 48611, q = 53993, form n = pq = 2624653723, and let X = {1,2,3,... ,n − 1}. Define a function f on X by f(x) = rx for each x ∈ X, where rx is the remainder when x3 is divided by n. For instance, f (2489991) = 1981394214 since 24899913 = 5881949859 · n + 1981394214. Computing f (x) is a relatively simple thing to do, but to reverse the procedure is much more difficult.

**Trapdoor one-way functions:** A trapdoor one-way function is a one-way function f : X −→ Y with the additional property that given some extra information (called the trapdoor information) it becomes feasible to find for any given y ∈ Im(f), an x ∈ X such that f(x) = y.