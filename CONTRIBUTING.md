# Contributing

We welcome contributions to the Awesome Agent APIs list.

## Suggesting an API

To suggest an API for inclusion:

1. The API must have a publicly available OpenAPI specification
2. Score it using the [Jentic API Scorecard CLI](https://github.com/jentic/jentic-api-scorecard):
   ```bash
   npx @jentic/api-scorecard-cli@latest score <path-or-url-to-spec>
   ```
3. Only APIs scoring **B- (60) or above** are eligible
4. Open an issue with:
   - API name and vendor
   - Link to the OpenAPI spec
   - Your scorecard output (overall score + grade)
   - Which category it belongs to

## Reporting a score issue

If you believe a score is inaccurate (e.g., the spec has been updated since scoring):

1. Open an issue with the API name and a link to the current spec
2. We'll re-score and update the list if the threshold is met

## Categories

If you think a new category is needed, open an issue to discuss before submitting a PR.

## Code of Conduct

Be respectful. This is a community resource.
