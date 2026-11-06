# Roadmap & Upstream Integration Plan: devtodo2-estimates

## Project Overview & UX Rationale
`devtodo2` is a lightweight command-line task management tool designed for quick, terminal-native hierarchical TODO tracking directly within project directories. By coupling task organization with local codebases, project plans archive cleanly alongside project source code (Credit to original UX design by Alec Thomas).

## Past Contributions (`razvan.coca@gmail.com`)
This repository branch introduces **recursive task estimation** to the core `devtodo2` paradigm:
- **Hierarchical Estimation Rollup:** Parent tasks automatically aggregate completed and pending estimates from child tasks.
- **Selective Estimation:** Unestimated tasks and branches remain uncalibrated without breaking tree calculations.
- **Full History Provenance:** All functional estimation logic and enhancements are committed under `razvan.coca@gmail.com`.

---

## Sandbox & Compliance Context
This repository (`rcoca-l/devtodo2-estimates`) serves as a public sandbox environment to audit, refactor, and align custom recursive estimation features with upstream evolution while maintaining strict software license compliance under the **Apache 2.0 License**.

---

## Upstream Integration & Refactoring Roadmap

### Phase 1: Baseline Drift Audit & Diff Mapping
- [ ] Map code structural drift between the original baseline and current `devtodo2` upstream updates.
- [ ] Identify breaking API changes in core AST handling, CLI flag parsing, and task tree serialization.
- [ ] Establish automated unit test baselines for hierarchical estimation logic.

### Phase 2: Core Semantic Porting
- [ ] Port task metadata data structures (estimate attributes) into upstream model primitives.
- [ ] Re-implement recursive parent/child aggregation functions using upstream-compatible traversal patterns.
- [ ] Ensure non-estimated tasks gracefully pass through rollup evaluations without introducing zero-value side effects.

### Phase 3: CLI Interface & Serialization Sync
- [ ] Re-align terminal output formatting and display flags for task estimates with upstream UX.
- [ ] Update disk serialization routines to guarantee backward and forward compatibility with standard `.todo` storage formats.
- [ ] Verify clean execution under standard Go toolchain builds (`go build`, `go test`).

### Phase 4: Validation & Upstream Merge Readiness
- [ ] Run complete end-to-end regression tests across nested task hierarchies.
- [ ] Cleanly isolate feature patches into atomic, reviewable commits for seamless upstream PR submission.
