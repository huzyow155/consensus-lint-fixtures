# ConsensusLint Fixtures

Public test fixture repository containing original GenLayer Intelligent Contracts used as audit targets for ConsensusLint on GenLayer Studionet (Preview).

## Fixtures Catalogue

- `bad_contract.py`: Intentionally violates structural and heuristic hygiene rules (CL01-CL03, CL05-CL18) for diagnostic testing.
- `good_contract.py`: Follows GenLayer consensus hygiene best practices (pinned header, ASCII, lazy init, validator recomputation, closed-enumeration comparisons, chain clock, UserError, bounded inputs, paginated views). Scores Grade A.
- `mixed_contract.py`: Realistic contract with a small number of common consensus-hygiene issues (unbounded parameter, unpaginated view, URL prefix check).
- `not_a_contract.py`: Utility module without a `gl.Contract` class (evaluates mode `NOT_A_CONTRACT`).
- `shell_like.py`: Oversized contract fixture (>60 KB) used to verify body truncation and B-grade capping.
- `evolving_contract.py`: Contract updated across commits to demonstrate mutable ref tracking and progress diffing (`get_progress`).
