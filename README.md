# Carnegie Peer Scorer

A single-page tool that scores every institution in the 2025 Carnegie Classifications against a chosen focal institution, using the five components of WSCUC's Key Indicators Dashboard peer methodology (Institutional Classification, control, Student Access and Earnings, size, and Research Activity Designation) as a weighted similarity profile rather than an exact-match filter.

It exists to prototype an edge-case tier for hierarchical peer assignment: when exact matching produces groups that are too large, label-only, or empty, similarity scoring with transparent weights and adjacency rules can produce a defensible peer group from the same public data.

## Use it

Open `index.html` in any browser, or visit the hosted page. There is no backend, no build step, and no tracking; the Carnegie data is embedded in the file.

Pick a focal institution, adjust the five component weights or use the presets, set the group size (10 to 30), and read each candidate's five-cell match pattern: full credit for an exact component match, half credit for an adjacent category, none otherwise.

## Scoring rules

- Classification: exact match full credit; half credit for the same classification family, for two institutions both carrying Carnegie's medical-school flag, or, within Special Focus, for two health categories (Medical Schools and Centers, Nursing, Other Health Professions).
- Control: exact; both-private pairs get half credit.
- Student Access and Earnings: both axes matched is full credit, one axis half; any pairing involving an unclassified institution scores half, treating missing data as unknown rather than as a match.
- Size: half credit one band apart.
- Research: half credit one designation step apart (R1, R2, RCU, none).
- Eligibility guard (on by default): a candidate with a different classification qualifies only when its health-professions status matches the focal institution's, preventing topical drift when classification weight is reduced.

Weights are policy choices made visible for discussion. The two presets are the proposal's defaults (40/20/15/15/10) and a cross-classification emphasis (25/20/15/20/20).

## Data

2025 Carnegie Classifications Public Data File (October 10, 2025 release) and 2025 Research Activity Designation Public Data File, American Council on Education and the Carnegie Foundation for the Advancement of Teaching, carnegieclassifications.acenet.edu. Institutions are identified by IPEDS UnitID.

Loma Linda University is the default worked example; its badges reflect LLU's peer group in WSCUC's Key Indicators Dashboard.

## Status and disclaimer

Independent prototype by Ken Nelson, Office of Educational Effectiveness, Loma Linda University. Not affiliated with, endorsed by, or an official product of ACE, the Carnegie Foundation, or WSCUC. Feedback welcome: wknelson@llu.edu.

## License

MIT for the code in this repository. The Carnegie public data files are published by ACE/Carnegie; consult their site for data reuse terms.
