# Detection Lifecycle

Detections should be treated as living artifacts, not permanent rules.

## 1. Design

- Define the behavior being detected
- Identify required signals
- State assumptions explicitly

## 2. Validation

- Test against known benign and malicious cases
- Validate signal availability
- Review false positives intentionally

## 3. Deployment

- Deploy with defined ownership
- Document expected behavior
- Set review checkpoints

## 4. Monitoring

- Track firing rate and noise trends
- Re-evaluate assumptions as environments change
- Monitor signal health

## 5. Retirement

- Remove detections that no longer provide value
- Retire rules with persistent noise
- Archive logic with rationale

A detection that cannot be safely maintained should not exist.
