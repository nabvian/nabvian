# Koushik Das

Independent researcher and systems architect. Built in India, for the world.

My work asks one question at every layer of a medical system: can this result
be trusted, and does the system know when it can't?

## The layers

**Knowledge.** Domain-blind reasoning engines for pathology, radiology,
oncology and rare disease. The engine knows nothing about medicine; the
medicine lives in knowledge a clinician can read, check and correct. Nothing is
guessed: every threshold and code traces to a source, and missing evidence is
reported as missing.
Public: [orphara-engine](https://github.com/nabvian/orphara-engine),
[caretrace-core](https://github.com/nabvian/caretrace-core)

**Learning (EG).** Rules alone don't read a blood smear or an X-ray; learned
models do, and a model can be confidently wrong on data from a hospital it has
never seen, with no internal warning. EG, evidence-gated networks, lets
evidence flow only when it is valid for the path it takes, and carries
reliability separately from prediction so that failure shows up instead of
hiding. It is a research hypothesis with a preregistered test that can reject it.

**Application (DMOS).** Where EG meets real data: structural findings from
blood smears. Private until clinically validated, because opening an
unvalidated medical tool is a risk, not a contribution.
Repository: [dmos-blood-smear](https://github.com/nabvian/dmos-blood-smear)
(private; access for reviewers and collaborators on request)

**Growth (UMNA).** A system that covers more medicine keeps gaining
capabilities, and each addition must not silently change what already worked.
UMNA keeps a frozen core, adds capabilities as versioned modules, routes
between them under hard budgets, and abstains when it isn't sure. Working
prototype; its hypotheses are not yet independently established.
Public: [umna-benchmarks](https://github.com/nabvian/umna-benchmarks)

**Computation (Q-BenchMed, BioCompute).** Before a new kind of computer is
trusted with a medical decision, it should be measured. Q-BenchMed gives
quantum optimisation and classical solvers the identical biomarker-selection
problem and reports what happens, including where quantum loses. Its latest
result: a constrained quantum ansatz beat a random valid answer on every
instance tested, where standard QAOA almost always lost to one. BioCompute goes
further out: computing inside molecules, compiling programs into chemical
reaction networks and checking the answers read back from noisy measurements
against an independent reference. Q-BenchMed runs in simulation; BioCompute is
at model-level proof of concept.
Public: [qbenchmed](https://github.com/nabvian/qbenchmed)

## Currently

- Taking Q-BenchMed's constrained-mixer experiment from simulation onto real
  quantum hardware, where two-qubit noise will decide whether its advantage
  survives.
- Moving UMNA from prototype to preregistered validation on real models.
- Extending the rare-disease engine's knowledge across haematology.

## How we work

I design the architecture and lead the research. My team writes and tests the
code, so the person who designs a system is never the only one certifying it.

Results are published as they come out, including the negative ones and my own
mistakes. Each project states its stage plainly: specification, prototype, or
validated. Engines are open source under AGPL; clinical components open after
validation.

## Collaboration

I'm looking to work with:

- clinicians and pathologists willing to review medical knowledge before it is
  used;
- hospitals and laboratories with data from sites a model has never seen, which
  is the test EG exists to pass;
- researchers with access to quantum hardware;
- funders who back open, independently checkable work.

Email: engikd1993@gmail.com
