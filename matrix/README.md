# ROOTED specialty matrices (canonical)

Authority level: operational registry (non-binding; the live database enforces). One truth model per section:

| Section | Model | Readable matrix |
|---|---|---|
| Agriculture | `agriculture/specialties.json` | `agriculture/ROOTED_SPECIALTY_MATRIX_AGRICULTURE.md` |

Each kind of business: its role (seller, buyer, both, place, nonprofit), the groups it belongs to, what it may do (shop, bulk
market, RFQ bids, public-buyer quotes, waste, events, field trips), the highest plan, what it sells (perishable, cold chain,
high-risk food, alcohol, live animals, visitors on site), how long buyers have to check its orders, and the papers it must
show before going live: required now (read from the live database) and required target (the plan).

How it is kept true: the private platform repository builds the readable matrix, a CSV and the database requirements
migration from the same model (`docs/specialty-matrix/build.py`), and `build.py --check` fails when the files or the last
live read disagree with the model. Change the model, rebuild, then publish the public copy here (without the per-type gaps,
which stay private).
