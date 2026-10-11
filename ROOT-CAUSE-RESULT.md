Fixed and reproduced: cron inherited the gateway’s **revoked stdin**, causing Python to fail before script execution. Script and Bot Chat launchers now receive `DEVNULL` stdin.

- Five regressions failed before and pass after.
- Final selection: **81 passed, 1 skipped**. Five broader failures also reproduce on baseline.
- Live jobs and services untouched.
- Commit blocked by sandbox access to shared Git metadata.

[Diagnosis and deployment procedure](/Users/cedricmuberuka/Developer/hermes-cron-stdio-fix/ROOT-CAUSE-RESULT.md) · [Apply-ready patch](/tmp/hermes-cron-stdio-review.patch)