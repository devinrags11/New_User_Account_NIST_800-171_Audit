# New_User_Account_NIST_800-171_Audit
## Objective
To verify "Least Privilege" (NIST 3.1.5) and prove that security controls are enforced system-wide and
cannot be bypassed by non-administrative users.
## Setup
* **Account Type:** Standard User (Non-Admin).
* **Scope:** Identity and Access Management (IAM) Validation.
## Audit Steps
1. **Provisioning:** Created a "Standard" user account via System Settings to simulate a typical employee
proile.
2. **Persistence Testing:** Logged in as the Standard user and attempted to revert security settings (e.g.,
disabling Firewall or Screen Lock).
3. **Verification:** Ran the mSCP audit script to identify which controls are "User-Specific" versus
"System-Wide."
## Findings
* **Vulnerability:** Identified that certain UI-based settings revert to defaults for new proiles unless
enforced via `/Library/Managed Preferences`.
* **Remediation:** Confirmed that `.mobilecon!g` proiles are required for consistent enforcement across
all user stubs.
