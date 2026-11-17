# SFCD 6 (candidate build)

Based on the supplied SFCD5 main ZIP.

## Changes
- New ministry role names and descriptions from supplied Word document (18 nomination slots).
- Reorganized admin dashboard with section navigation and collapsible panels.
- Admin voter reset (closed elections only); will refuse if anonymous phase ballots exist for the voter.
- Admin full test election reset clears all phase ballots, participation, and ministerial submissions for one closed election. Preserves registered voters and election configuration.
- Existing SFCD5 ministerial data is NOT silently relabeled as new roles. Legacy rounds with nominations require explicit migration or full test reset.

## Important
This is a development candidate, NOT deployed or production validated. Back up the live SQLite database and uploaded files before any migration. Test with a COPY of production data, not live election data. Old ministry nominations are indexed by role order; role names have changed. Do not re-label historical results.

Individual anonymous votes cannot be identified for removal. Use full test election reset before live voting, not an individual reset.

## Install
Use a fresh working directory/branch. Keep production SFCD5 running until tested. Review environment variables, secrets, database path, and reverse proxy before deployment.
