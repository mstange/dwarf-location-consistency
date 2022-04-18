# dwarf-location-consistency

In some Rust executables we're seeing DWARF debug data where the debug line info is not consistent with the inline_subprogram info: There exist addresses for which the innermost inline_subprogram is declared in source file A, but the debug line info gives source file B for that same address.

This repo is intended to host a tool to check for such inconsistencies.

At the moment the code here is just a straight up copy of the Rust addr2line crate + example.
