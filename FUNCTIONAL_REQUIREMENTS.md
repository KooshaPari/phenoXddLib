# Functional Requirements — phenotype-xdd-lib

## FR-PROP — Property Testing

| ID | Requirement |
|----|-------------|
| FR-PROP-001 | The library SHALL provide proptest strategies for common Phenotype domain types. |
| FR-PROP-002 | The library SHALL provide composable strategy builders for nested domain structures. |
| FR-PROP-003 | All custom strategies SHALL support proptest shrinking. |

## FR-CONTRACT — Contract Testing

| ID | Requirement |
|----|-------------|
| FR-CONTRACT-001 | The library SHALL provide a port verification framework for hexagonal adapters. |
| FR-CONTRACT-002 | The library SHALL provide a contract_test macro that generates conformance test suites. |
| FR-CONTRACT-003 | Contract test failures SHALL produce diagnostics naming the mismatched method and expected behavior. |

## FR-MUTANT — Mutation Testing

| ID | Requirement |
|----|-------------|
| FR-MUTANT-001 | The library SHALL provide coverage tracking utilities compatible with cargo-mutants. |
| FR-MUTANT-002 | The library SHALL report mutation kill rate per module. |
| FR-MUTANT-003 | The library SHALL provide CI integration hooks for mutation threshold gates. |

## FR-SPEC — SpecDD

| ID | Requirement |
|----|-------------|
| FR-SPEC-001 | The library SHALL parse FR IDs from Markdown specification documents. |
| FR-SPEC-002 | The library SHALL validate that test functions reference known FR IDs. |
| FR-SPEC-003 | The library SHALL report orphan tests (no FR reference) as warnings. |
| FR-SPEC-004 | The library SHALL report uncovered FRs (no test reference) as warnings. |
