# Unsafe Rust Pointer Manipulation Leading to Vector Corruption

This repository demonstrates a potential issue with unsafe Rust code involving raw pointers and vector manipulation.  The `bug.rs` file contains code that directly modifies a vector's internal data using a raw pointer. This approach is unsafe and can lead to data corruption, memory leaks, or panics if not handled correctly.  The `bugSolution.rs` shows a safer alternative using safe Rust methods.

**Potential Problems:**

* **Data Corruption:** Modifying the vector's contents through the raw pointer without proper bookkeeping can corrupt the vector's internal state.
* **Memory Leaks:** If memory management isn't carefully handled, this approach can lead to memory leaks.
* **Undefined Behavior:** The behavior of the code is undefined if the raw pointer is not correctly managed, possibly causing crashes or other unpredictable issues.

**Solution:**

The safer alternative demonstrated in `bugSolution.rs` uses Rust's safe methods for vector manipulation, avoiding the risks associated with unsafe code.