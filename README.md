# New_User_Account_NIST_800-171_Audit
## Objective
To verify "Least Privilege" (NIST 3.1.5) and prove that security controls are enforced system-wide and
cannot be bypassed by non-administrative users.
## Setup
* **Account Type:** Standard User (Non-Admin).
* **Scope:** Identity and Access Management (IAM) Validation.
## Audit Steps
1. **Provisioning:** Created a "Standard" user account via System Se"ings to simulate a typical employee
pro!le.
2. **Persistence Testing:** Logged in as the Standard user and a"empted to revert security se"ings (e.g.,
disabling Firewall or Screen Lock).
3. **Veri!cation:** Ran the mSCP audit script to identify which controls are "User-Speci!c" versus
"System-Wide."
## Findings
* **Vulnerability:** Identi!ed that certain UI-based se"ings revert to defaults for new pro!les unless
enforced via `/Library/Managed Preferences`.
* **Remediation:** Con!rmed that `.mobilecon!g` pro!les are required for consistent enforcement across
all user stubs.
