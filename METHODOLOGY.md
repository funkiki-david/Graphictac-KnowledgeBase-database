# Methodology

## Objective

The dataset organizes source-linked information that helps print shops research printable media and printer workflows without turning preliminary research into unsupported certification claims.

## Source selection

Priority is given to:

1. Official manufacturer product pages.
2. Official technical bulletins or product information bulletins.
3. Brand-controlled application or workflow pages.

Secondary commentary is not used as the sole support for a technical compatibility statement in this release.

## Collection and normalization

- A researcher records the source URL, brand or topic, workflow context, and intended use.
- Product and printer family names are preserved as written by the source when practical.
- Multi-value fields use semicolon-separated values in CSV and remain strings in JSONL.
- Source review dates use ISO `YYYY-MM-DD` format.
- Missing values are left blank rather than inferred.

## Claim-risk labels

- `High`: exact performance, warranty, certification, equivalency, durability, or cross-brand compatibility should be verified before publication.
- `Medium`: official source context exists, but application-specific performance still requires current documentation and testing.
- Blank: the source library does not assign a claim-risk score.

## Quality controls

- CSV files must have a stable header and consistent column count.
- JSONL output must contain one valid JSON object per non-empty line.
- Source URLs must use HTTP or HTTPS.
- Dataset row totals must reconcile with the release manifest.
- Technical compatibility is described as workflow context unless the cited source explicitly supports a stronger claim.

## Update policy

This release is a dated snapshot. Future releases should:

1. Recheck source availability and product status.
2. Record changed URLs or specifications.
3. Preserve prior tagged releases for auditability.
4. Increment the dataset version and publish a changelog.

## Responsible use

Users should confirm current manufacturer documentation, ICC/profile requirements, ink compatibility, laminate pairing, surface preparation, and application conditions. Production samples and controlled testing remain necessary.
