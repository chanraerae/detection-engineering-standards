# Detection Quality Standards

A detection is only useful if it can be trusted during real incidents.

High volume or frequent firing does not imply quality.

## 1. Behavioral Alignment

A detection should map to attacker behavior rather than a single tool or indicator.

Questions to ask:
- What behavior is being detected?
- Would this still fire if the attacker changed tooling?
- What assumptions does this detection make?

Failure modes:
- Tool-specific logic
- Static indicators without context
- Overfitting to past incidents

## 2. Signal Inputs

Detections should clearly state which signals they rely on.

Questions to ask:
- Are signals reliable and consistently available?
- What happens if one signal drops?
- Are signals correlated or independent?

Failure modes:
- Hidden dependencies
- Implicit enrichment
- Missing telemetry awareness

## 3. Noise and Precision

A detection should justify its noise level.

Questions to ask:
- What is an acceptable false positive rate?
- Who absorbs the cost of investigation?
- How is noise monitored over time?

Failure modes:
- Alert fatigue
- No tuning ownership
- Noise treated as normal

## 4. Explainability

A detection should be explainable to someone on call.

Questions to ask:
- Can the logic be explained without referencing code?
- Is the alert message actionable?
- Can a responder explain why it fired?

Failure modes:
- Opaque scoring
- Black-box logic
- Alert text that repeats field names

## 5. Operational Safety

A detection should be safe to act on.

Questions to ask:
- What actions might this trigger?
- What is the risk of acting incorrectly?
- Is human validation required?

Failure modes:
- Over-automated responses
- High-impact actions without confidence
- No rollback considerations
