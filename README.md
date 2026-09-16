# repo_snl-marketing-sales

Automated follow-up tracking for SNL marketing & sales meetings captured in Krisp.

A scheduled Claude task checks Krisp every 2 hours for new meetings and:

- Creates one GitHub Issue per new meeting (summary + action items), tagged with the Krisp meeting ID in the body for dedup
- Updates `PLANBOARD.md` with the current state of all open follow-ups
- Emails Stefan a run summary

Issues are closed manually (or by future automation) once action items are done; closing an issue removes it from the active planboard on the next run.
