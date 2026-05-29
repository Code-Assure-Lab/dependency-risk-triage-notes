Dependency Risk Triage Notes
Notes and templates for evaluating vulnerable software dependencies in a
defensive engineering workflow.

The goal is to help teams decide whether a dependency finding is reachable,
urgent, and safely remediable without creating unnecessary operational risk.

Triage Questions
For each dependency alert, capture:

Package name and ecosystem
Current version and recommended fixed version
Advisory source and identifier
Affected feature or component
Whether the vulnerable code path is reachable
Exposure context: internal, authenticated, public, or build-time only
Available upgrade path
Compatibility or regression concerns
Proposed remediation owner and timeline
Reachability Notes
Reachability analysis should focus on application behavior:

Is the affected package imported or bundled?
Is the vulnerable function, parser, handler, or protocol path used?
Can untrusted input reach that path?
Are there framework-level mitigations or configuration controls?
Does the vulnerable behavior apply to the deployed version and platform?
Remediation Options
Common remediation paths:

Upgrade to the fixed version.
Apply a vendor-supported patch.
Disable or remove the vulnerable feature.
Add configuration-level mitigation where supported.
Replace the dependency when maintenance risk is high.
Temporary mitigations should be documented with an owner and expiration date.

Review Template
Package:
Current version:
Fixed version:
Advisory:
Affected component:
Reachable: yes / no / unknown
Exposure:
Recommended action:
Regression risk:
Owner:
Target date:
Validation notes:
Responsible Use
These notes are intended for defensive dependency review on owned or authorized
software systems. They are not intended to support exploitation, unauthorized
testing, or data access against third-party systems.
