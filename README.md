# DARRT Deterministic C++ AI Runtime for Real Time Systems

A lightweight, deterministic, secure and safe C++ runtime designed for memory-constrained, real-time, and heterogeneous compute environments, with support for CPU, GPU, and AI accelerator abstraction across SoCs.

## Overview

This project provides a unified runtime layer that bridges:

1. Low-level OS primitives
2. Parallel compute execution
3. AI inference across heterogeneous hardware

The goal is to enable:

> Predictable, portable, and efficient execution of compute and AI workloads without dynamic memory overhead in a safe and secure environment.

## Core Features

#### Deterministic Design
* No dynamic memory allocation (heap-free core)
* Compile-time bounded data structures
* Predictable execution and latency

#### Memory-Safe Containers
* Fixed-capacity containers
* static_vector, fixed_string, etc.
* No heap usage, no fragmentation

#### OS Abstraction Layer (POSIX)
* Thin abstraction over POSIX APIs
* Thread, mutex, synchronization primitives
* Designed for portability (Linux → RTOS-ready)

#### Restricted Runtime
* No exceptions (```-fno-exceptions```)
* No RTTI (```-fno-rtti```)
* Suitable for embedded and safety-critical systems

#### Configurable Memory Model
* Preallocated buffers
* Optional memory pools
* Deterministic allocation strategies

#### Parallel Compute Abstraction
* Unified compute interface across:
    * CPU (thread-based parallelism)
    * GPU (future backend)
* parallel_for execution model
* Deterministic scheduling

#### AI Runtime Abstraction
* Unified interface for AI inference across SoCs
* Backend-agnostic execution (CPU/GPU/NPU)

#### Security & Safety
* No dynamic memory allocation (heap-free design)
* Bounds-checked containers
* Model integrity verification (hash-based)
* Explicit resource ownership
* Restricted runtime (no exceptions, no RTTI)

#### Safety Guarantees
* Deterministic execution and memory usage
* Compile-time resource limits
* Fail-safe error handling (no exceptions)
* Watchdog-based execution timeout
* Thread-safe design

Supports:

1. Load model
2. Run inference
3. Manage memory
4. Switch backend (CPU / GPU / NPU)
5. Unload cleanly

Backend example:

* ONNX Runtime (CPU backend)

## Architecture

| Layer         | Description |
| ------------- |:-------------:|
| AI Runtime    | Model loading - Inference execution - Backend selection |
| Compute       | Compute Abstraction (CPU / GPU) |
| Platform      | OS Abstraction     |




## Key Advantages

##### Determinism

* Predictable latency
* No heap-related jitter

##### Portability

* POSIX-based abstraction
* Extendable to RTOS (QNX, VxWorks)

##### Real-Time Safety

* No exceptions
* No dynamic allocation
* Bounded execution

##### Advanced Memory Management

* Preallocated tensors
* Zero-copy design (where possible)
* Cross-device memory handling

##### Data Layout Awareness

* Handling NCHW vs NHWC
* Handling Quantized vs floating-point tensors

##### Device Selection

* Explicit backend control:

## Measurements & Benchmarking

#### Latency TBD
#### Memory TBD
#### Stack TBD 
#### Memory Safety TBD
#### Determinsm TBD
#### Fault Injection TBD
#### Time Enforcement TBD

## Roadmap

#### Current
1. Deterministic containers
2. POSIX OS abstraction
3. CPU parallel execution
4. AI inference (CPU backend)
#### Planned
1. GPU backend (CUDA / Vulkan)
2. RTOS support (QNX, VxWorks)
3. Advanced memory pools
4. Static inference planning
5. Zero-copy tensor pipelines

## USP

* Deterministic execution
* Embedded-friendly design
* Clean C++ systems abstraction
* Unified compute + AI runtime
* Minimal abstraction (no hidden cost)
* Explicit memory control
* Compile-time over runtime
* Measure everything

## License
Refer the licence file.