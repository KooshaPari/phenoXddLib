# PRD — phenotype-xdd-lib

## Overview

`phenotype-xdd-lib` is a cross-cutting Rust library implementing xDD (eXtreme Domain-Driven) utilities: property testing strategies, contract testing for hexagonal ports, mutation testing coverage tracking, and specification parsing/validation.

## Goals

- Provide reusable testing primitives that enforce xDD methodologies across all Rust projects in the Phenotype ecosystem.
- Reduce boilerplate in property tests, contract tests, and mutation tracking.
- Validate specifications programmatically against domain contracts.

## Epics

### E1 — Property Testing
- E1.1 Provide proptest strategies for common Phenotype domain types.
- E1.2 Composable strategy builders for nested domain structures.
- E1.3 Shrinking support for all custom strategies.

### E2 — Contract Testing
- E2.1 Port verification framework: given a port interface, assert adapter conformance.
- E2.2 Macro `#[contract_test]` that generates conformance test suites.
- E2.3 Report port/adapter mismatches with actionable diagnostics.

### E3 — Mutation Testing
- E3.1 Coverage tracking utilities compatible with `cargo-mutants`.
- E3.2 Mutation kill rate reporter per module.
- E3.3 Integration hooks for CI mutation gates.

### E4 — SpecDD
- E4.1 Parse spec documents (FR, PRD) into structured Rust types.
- E4.2 Validate that test functions reference FR IDs.
- E4.3 Report orphan tests (no FR) and uncovered FRs (no test).

## Acceptance Criteria

- Property tests using xdd-lib strategies compile and run with proptest 1.x.
- `#[contract_test]` generates a passing test suite for a correctly implemented adapter.
- SpecDD parser extracts FR IDs from Markdown and cross-references them to test annotations.
