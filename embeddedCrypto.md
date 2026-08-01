# Guiding principle

* C++
* DSA
* Cryptography

> **Writing high-quality cryptographic software in modern C++ for embedded systems.**

---

## Weekly Schedule

| Day       | Time | Focus                                     | Book                                   |
| --------- | ---- | ----------------------------------------- | ---------------------------------------|
| Monday    | 2 h  | Cryptography (Theory)                     | **Serious Cryptography**               |
| Tuesday   | 2 h  | DSA                                       | **Wengrow** + **Karumanchi**           |
| Wednesday | 2 h  | Cryptography (Internals)                  | **Understanding Cryptography**         |
| Thursday  | 2 h  | DSA                                       | **Wengrow** + **Karumanchi**           |
| Friday    | 2 h  | Cryptography (Implementation & Standards) | **Real World Cryptography**            |
| Saturday  | 4 h  | C++ Course (≈1 lecture + notes)           | 1 Lecture                              |
| Sunday    | 4 h  | C++ exercises + concept application       | **Effective Modern C++** (1 item/week) |

---

## Monday - Cryptography (Theory)

**Primary book:** ***Serious Cryptography***

Goal: ***Understand **what** an algorithm does and **why** it exists.***

Examples:

* AES
* SHA-256
* HMAC
* HKDF
* ECDSA
* Certificates

Ask questions like:

* Why is AES-GCM preferred over AES-CBC?
* Why is nonce reuse catastrophic?
* Why is HKDF needed?

Take notes in your own words.

---

## Tuesday - DSA

Use both books together.

### 20-30 min

* Read ***Wengrow***
* Understand the intuition.

### 30-40 min

* Read ***Karumanchi***
* See how it's implemented.

### 50-60 min

* Close both books.
* Implement everything yourself.
* No copying.

---

## Wednesday - Cryptography (Internals)

**Primary book:** ***Understanding Cryptography***

Stay on the same topic as Monday.

Example:

| Monday | → | Wednesday                                                        |
|--------|---|------------------------------------------------------------------|
| AES    | → | Finite Fields<br> Rijndael S-box<br>Mix Columns<br>Key Expansion |

This will make it clear how AES actually works. This is the difference between *using* cryptography
and *implementing* cryptography.

---

## Thursday - DSA

Continue implementing.

* write tests
* benchmark
* improve design
* solve a couple of problems

Spend **two weeks per topic**. Quality > quantity.

---

## Friday - Cryptography (Implementation)

Rotate between:

* **Real-World Cryptography**
* NIST standards
* RFCs
* Reading mbedTLS/BoringSSL/OpenSSL
* Small implementations

| Week 1         | Week 2        | Week 3               | Week 4                     |
|----------------|---------------|----------------------|----------------------------|
| Implement HKDF | Read RFC 5869 | Compare with mbedTLS | Write tests and benchmarks |

This is the highest-value session because it connects theory with production code.

---

## Saturday - C++ Course

Watch approximately **one lecture** (3.5 hours).

Don't rush. Take notes. This course is a long term investment.

---

## Sunday - Apply the C++

* Complete exercises from Saturday.
* Refactor your DSA implementations.
* Improve your crypto code.

Examples:

Lecture:

Templates

↓

Convert

```cpp
Stack<int>
```

into

```cpp
template<typename T>
class Stack
```

Lecture:

Move semantics

↓

Improve

```cpp
Vector
```

Lecture:

Smart pointers

↓

Rewrite ownership.

Lecture:

`constexpr`

↓

Improve compile-time utilities.

This will turn the C++ course into practical skill.

---

## Where each book fits

| Book                           | Purpose                    | When                 |
| ------------------------------ | -------------------------- | -------------------- |
| **Serious Cryptography**       | Practical crypto concepts  | Monday               |
| **Understanding Cryptography** | Crypto internals           | Wednesday            |
| **Real-World Cryptography**    | Protocols & systems        | Friday               |
| **Wengrow**                    | Build intuition            | Tuesday              |
| **Karumanchi**                 | Learn implementation       | Tuesday & Thursday   |
| **Effective Modern C++**       | Modern C++ best practices  | Sunday (1 item/week) |
| **Pragmatic Programmer**       | Engineering habits         | Casual reading       |
| **Hacker's Delight**           | Bit manipulation reference | As needed            |
| **C++ Concurrency in Action**  | Advanced C++               | After the C++ course |

---

## Effective Modern C++

This is the "slow book."

Read **one Item per week**.

Then immediately apply it.

Example:

> Read an Item on move semantics.
>
> ↓
>
> Improve your `Vector`.

> Read an Item on `auto`.
>
> ↓
>
> Review your codebase.

> Read an Item on smart pointers.
>
> ↓
>
> Improve ownership.

**Never binge-read this book.**

---

## Pragmatic Programmer

Read 10-20 pages before bed.

Think:

> "Can this idea be applied at work tomorrow?"

---

## Hacker's Delight

This book is not meant to be studied sequentially.

Instead, when you encounter something like the following:

* ```cpp
  x &= x - 1;
  ```

* ```cpp
  std::rotl(x, n)
  ```

* a branchless comparison,

look up the relevant chapter.

---

## C++ Concurrency in Action

After the course has covered:

* threads
* atomics
* memory model

Read one chapter every couple of weeks.

There's no benefit in reading it too early.

---

## One integrated repository

```text
embedded-crypto-roadmap/
├── cpp-foundations/
│   ├── graph/
│   ├── hashmap/
│   ├── heap/
│   ├── linked_list/
│   └── vector/
├── crypto/
│   ├── asymmetric/
│   │   ├── ecc/
│   │   │   ├── ed25519/
│   │   │   └── secp256r1/
│   ├── boot/
│   │   └── secure_boot/
│   ├── certificates/
│   │   └── x509/
│   ├── hash/
│   │   ├── blake2/
│   │   ├── sha256/
│   │   └── sha3/
│   ├── kdf/
│   │   ├── hkdf/
│   │   └── pbkdf2/
│   ├── mac/
│   │   ├── cmac/
│   │   └── hmac/
│   ├── protocols/
│   │   └── tls_handshake_demo/
│   ├── rng/
│   │   └── ctr_drbg/
│   ├── signature/
│   │   ├── ecdsa/
│   │   └── ed25519/
│   └── symmetric/
│       └── aes/
│           ├── cbc/
│           ├── ctr/
│           ├── ecb/
│           └── gcm/
├── playground/
├── benchmarks/
└── tests/
```

As your C++ skills improve, revisit older implementations instead of leaving them behind. That
demonstrates growth and mirrors how production software evolves.

---

## Long-term progression

### Months 1-3

#### DSA focus

* Vector
* Linked List
* Stack
* Queue
* Hash Table
* Heap

#### Crypto focus

* Hashes
* HMAC
* AES
* Modes of operation

---

### Months 4-6

#### DSA

* Trees
* Graphs
* Sorting
* Dynamic Programming (fundamentals)

#### Crypto

* ECC
* ECDSA
* HKDF
* Random number generation
* Certificates

---

### Months 7-12

Shift the emphasis toward embedded cryptography.

Build:

* SHA-256 implementation
* HMAC
* HKDF
* DER/ASN.1 parser
* X.509 parser
* Secure Boot demonstration
* Firmware signature verification

By this stage, DSA should become maintenance rather than my primary focus.

---

## Why this is the strongest plan

The objective isn't to become a generalist software engineer or a competitive programmer. It's to
become an **Embedded Cryptography Engineer**.

This schedule reflects that:

* **Cryptography** becomes my deepest area of expertise.
* **DSA** gives me the implementation confidence needed for interviews.
* **Modern C++** raises the quality of everything I write.
* **Engineering books** improve how yoI design, maintain, and reason about software.

The result is that, by the time I'm interviewing, I won't just be able to explain cryptographic
concepts—I'll be able to **implement them cleanly, test them rigorously, and express them in modern C++**,
which is exactly the combination many embedded security teams are looking for.
