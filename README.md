# Awesome Agent APIs [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of APIs that score highest for AI-agent readiness — evaluated using the [Jentic API AI-Readiness Framework (JAIRF)](https://github.com/jentic/api-ai-readiness-framework).

Not all APIs are created equal when it comes to AI agents. A valid OpenAPI spec doesn't mean an agent can understand, discover, or safely use it. This list highlights the APIs that are genuinely ready for autonomous agent use — based on measurable, reproducible scoring across six dimensions.

## Why Spec Quality Matters

MCPs (Model Context Protocol servers) exist for a handful of popular APIs. But:

- **MCPs cover ~50 APIs. There are 100,000+ APIs in the wild.** Your agent will encounter APIs without MCPs.
- **MCPs expose a curated subset** — typically 15-30 tools from APIs with hundreds of endpoints. The full surface requires reading the spec.
- **Coding agents read specs directly.** When Claude Code, Cursor, or Copilot generate integration code, they interpret the OpenAPI spec — not an MCP.
- **Your internal APIs don't have MCPs.** Enterprise teams with 50-200 internal microservices need their specs to be agent-interpretable as-is.

The APIs on this list have specs that agents can reason about effectively — clear semantics, good descriptions, consistent operation IDs, well-structured schemas, and appropriate complexity.

## Scoring

Every API is scored across six dimensions by the [Jentic API AI-Readiness Framework](https://github.com/jentic/api-ai-readiness-framework):

| Dimension | What it measures |
|-----------|-----------------|
| **Foundational Compliance** | Structural validity and standards conformance |
| **Developer Experience** | Documentation quality and tooling support |
| **AI-Readiness & Agent Experience** | Semantic clarity and context sufficiency for AI systems |
| **Agent Usability** | Safe, predictable multi-step operations |
| **Security** | Authentication, authorization, and trust mechanisms |
| **AI Discoverability** | How easily AI systems can find and understand the API |

**Grading:** A+ (90+) → F (<40). Only APIs scoring **B- (60) or above** make this list.

## Contents

- [AI & LLM Providers](#ai--llm-providers)
- [Search & Recommendations](#search--recommendations)
- [Project Management & Productivity](#project-management--productivity)
- [Cloud Infrastructure & DevOps](#cloud-infrastructure--devops)
- [Databases & Data Platforms](#databases--data-platforms)
- [Communication & Email](#communication--email)
- [Auth & Identity](#auth--identity)
- [Storage & Content](#storage--content)
- [CRM & Marketing](#crm--marketing)
- [Music & Media](#music--media)

---

## AI & LLM Providers

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Groq API](https://groq.com) | 68.29 | B+ | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/groq.com/main/1.0) |
| [Amazon Bedrock Runtime](https://aws.amazon.com/bedrock/) | 64.12 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/bedrock-runtime/2023-09-30) |
| [Algolia Recommend API](https://www.algolia.com/doc/rest-api/recommend/) | 63.40 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-recommend-api/1.0.0) |

## Search & Recommendations

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Algolia Insights](https://www.algolia.com/doc/rest-api/insights/) | 65.45 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-insights-api/1.0.0) |
| [Algolia Recommend](https://www.algolia.com/doc/rest-api/recommend/) | 63.40 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-recommend-api/1.0.0) |
| [Algolia Search](https://www.algolia.com/doc/rest-api/search/) | 61.08 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-search-api/1.0.0) |
| [Algolia Ingestion](https://www.algolia.com/doc/rest-api/ingestion/) | 60.99 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-ingestion-api/1.0.0) |

## Project Management & Productivity

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Figma REST API](https://www.figma.com/developers/api) | 68.97 | B+ | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/figma.com/figma-rest-api/1.0.0) |
| [ClickUp API](https://clickup.com/api) | 68.91 | B+ | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/clickup.com/clickup-api/2.0) |
| [Linear API](https://developers.linear.app) | 66.57 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/linear.app/main/1.0) |
| [Airtable Web API](https://airtable.com/developers/web/api) | 64.85 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/airtable.com/main/0.1.0) |

## Cloud Infrastructure & DevOps

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [AWS Lambda API](https://docs.aws.amazon.com/lambda/) | 66.85 | B | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/aws-lambda-api/2015-03-31) |
| [Neon API](https://neon.tech/docs/reference/api-reference) | 62.90 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/neon.tech/main) |
| [Docker Engine API](https://docs.docker.com/engine/api/) | 61.87 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/docker.com/engine/1.33) |
| [AWS CodeCommit](https://docs.aws.amazon.com/codecommit/) | 61.91 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/codecommit/2015-04-13) |
| [AWS RDS Data](https://docs.aws.amazon.com/rdsdataservice/) | 61.92 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/rds-data/2018-08-01) |
| [Amazon EKS](https://docs.aws.amazon.com/eks/) | 60.78 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/eks/2017-11-01) |
| [AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/) | 60.73 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/codepipeline/2015-07-09) |
| [AWS Step Functions](https://docs.aws.amazon.com/step-functions/) | 60.54 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/states/2016-11-23) |
| [Amazon CloudWatch Events](https://docs.aws.amazon.com/cloudwatch/) | 60.28 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/events/2015-10-07) |
| [AWS App Runner](https://docs.aws.amazon.com/apprunner/) | 60.30 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/apprunner/2020-05-15) |
| [Amazon Cognito Identity](https://docs.aws.amazon.com/cognito/) | 61.44 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/cognito-identity/2014-06-30) |

## Databases & Data Platforms

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Supabase Management API](https://supabase.com/docs/reference/api) | 70.46 | A- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/supabase.com/main) |
| [Neon API](https://neon.tech/docs/reference/api-reference) | 62.90 | B- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/neon.tech/main) |

## Communication & Email

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Resend](https://resend.com/docs/api-reference) | 54.68 | C | — |
| [SendGrid Mail API](https://docs.sendgrid.com/api-reference) | 59.57 | C+ | — |

> *Note: No communication APIs in our current sample meet the B- threshold. This category is a known gap — popular APIs like Slack (D), Twilio (F), and Discord (F) score poorly due to sparse descriptions and missing semantic context in their specs.*

## Auth & Identity

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Auth0 Authentication API](https://auth0.com/docs/api) | 68.77 | B+ | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/auth0.com/main/2.0.0) |

## Storage & Content

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Contentful Images API](https://www.contentful.com/developers/docs/references/images-api/) | 69.53 | B+ | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/contentful.com/main/1.0.0) |
| [Dropbox API v2](https://www.dropbox.com/developers/documentation) | 58.81 | C+ | — |

> *Note: Only Contentful meets the B- threshold in this category. Dropbox (C+) is close.*

## CRM & Marketing

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Sentry API](https://docs.sentry.io/api/) | 59.67 | C+ | — |
| [Intercom API](https://developers.intercom.com/docs) | 57.49 | C+ | — |

> *Note: No CRM/Marketing APIs in our sample meet the B- threshold. HubSpot CRM (D-), Salesforce, and Mailchimp (F) all score below the bar due to large surface area with poor semantic coverage.*

## Music & Media

| API | Score | Grade | Spec |
|-----|-------|-------|------|
| [Spotify Web API](https://developer.spotify.com/documentation/web-api) | 73.89 | A- | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/spotify.com/sonallux) |

---

## Notable APIs Below the Threshold

These APIs are widely used by agents but their specs currently score below B-. They represent opportunities for improvement:

| API | Score | Grade | Why it matters |
|-----|-------|-------|----------------|
| [OpenAI API](https://platform.openai.com/docs/api-reference) | 55.11 | C | The most-used LLM API |
| [Anthropic API](https://docs.anthropic.com/en/docs) | 59.54 | C+ | Close to threshold — strong agent usability (93.5) |
| [Stripe API](https://docs.stripe.com/api) | 51.37 | C- | The default payments API for agents |
| [GitHub REST API](https://docs.github.com/en/rest) | 37.39 | F | 900+ endpoints, minimal descriptions |
| [Slack Web API](https://api.slack.com/methods) | 46.27 | D | Sparse spec, low AI-readiness (27.5) |
| [Notion API](https://developers.notion.com) | 42.81 | D- | Very low agent usability (21.1) |
| [Google Gmail API](https://developers.google.com/gmail/api) | 20.87 | F | High agent usability (89.3) but near-zero AI-readiness (6.7) |
| [Twilio Messaging](https://www.twilio.com/docs/messaging/api) | 27.03 | F | Well-structured but lacks semantic richness |
| [Shopify Admin API](https://shopify.dev/docs/api/admin-rest) | 53.24 | C | Large surface with limited descriptions |

---

## Score Your Own APIs

Want to see how your APIs score for AI-agent readiness?

### Online

Upload your OpenAPI spec at **[jentic.com/scorecard](https://jentic.com/scorecard)** for an instant assessment across all six dimensions.

### CLI (local, no data sent to Jentic)

```bash
npx @jentic/api-scorecard-cli@latest score <path-or-url-to-openapi-spec>
```

### Learn more

- [API AI-Readiness Framework specification](https://github.com/jentic/api-ai-readiness-framework)
- [Jentic API Scorecard (CLI source)](https://github.com/jentic/jentic-api-scorecard)
- [Blog: API Scoring Tools](https://jentic.com/blog/api-scoring-tools)

---

## About

This list is maintained by [Jentic](https://jentic.com) and sourced from the [Jentic Public APIs](https://github.com/jentic/jentic-public-apis) catalogue — 7,400+ APIs scored for AI-agent readiness.

APIs are included based on their overall AI-readiness score (B- / 60+ threshold) and relevance to common agent use cases. Scores are generated automatically by the [Jentic API Scorecard](https://github.com/jentic/jentic-api-scorecard) using the [JAIRF specification](https://github.com/jentic/api-ai-readiness-framework).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on suggesting APIs or reporting score issues.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Jentic](https://jentic.com) has waived all copyright and related rights to this work.
