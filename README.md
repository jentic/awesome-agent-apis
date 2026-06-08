# Awesome Agent APIs [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of APIs whose OpenAPI specs are genuinely usable by AI agents — scored using the [Jentic API AI-Readiness Framework (JAIRF)](https://github.com/jentic/api-ai-readiness-framework).

Not all APIs are created equal when it comes to AI agents. A valid OpenAPI spec doesn't mean an agent can understand or use it. This list surfaces the APIs whose specs are best equipped for autonomous agent interaction — based on measurable, reproducible scoring.

## Why Spec Quality Matters

MCPs (Model Context Protocol servers) exist for a handful of popular APIs. But:

- **MCPs cover ~50 APIs. There are 100,000+ APIs in the wild.** Your agent will encounter APIs without MCPs.
- **MCPs expose a curated subset** — typically 15-30 tools from APIs with hundreds of endpoints. The full surface requires reading the spec.
- **Coding agents read specs directly.** When Claude Code, Cursor, or Copilot generate integration code, they interpret the OpenAPI spec — not an MCP.
- **Your internal APIs don't have MCPs.** Enterprise teams with 50-200 internal microservices need their specs to be agent-interpretable as-is.

The APIs on this list have specs that agents can reason about effectively — clear semantics, good descriptions, consistent operation IDs, well-structured schemas, and appropriate complexity.

## How We Score for This List

The full [JAIRF framework](https://github.com/jentic/api-ai-readiness-framework) evaluates APIs across six dimensions. For this list, we focus on the two that directly answer **"can an agent understand and use this API?"**:

| Dimension | What it measures |
|-----------|-----------------|
| **Agent Usability (AU)** | Can an agent safely execute multi-step operations? Considers complexity comfort, endpoint count, schema depth, and orchestration readiness. |
| **AI-Readiness & Agent Experience (ARAX)** | Can an agent *understand* what the API does? Measures description coverage, semantic richness, operation ID quality, and summary clarity. |

### Agent Effectiveness Score

We use the **Agent Effectiveness Score** = average of AU and ARAX:

```
Agent Effectiveness Score = (Agent Usability + AI-Readiness) / 2
```

**Threshold: 60+** to make this list.

### Why not the overall score?

The full JAIRF score also includes Security, Foundational Compliance, Developer Experience, and AI Discoverability. These matter for governance and tooling — but they don't tell you whether an agent can *use* the API. An API with simple API-key auth (scored lower on Security) is often *easier* for an agent to use than one requiring complex OAuth flows. A spec with linting warnings (lower Foundational score) can still be perfectly interpretable by an agent.

We focus on what agents actually need: **can they understand it (ARAX) and can they operate it safely (AU)?**

## Contents

- [AI & LLM Providers](#ai--llm-providers)
- [Search & Recommendations](#search--recommendations)
- [Project Management & Productivity](#project-management--productivity)
- [Cloud Infrastructure & DevOps](#cloud-infrastructure--devops)
- [Databases & Data Platforms](#databases--data-platforms)
- [Communication & Email](#communication--email)
- [Monitoring & Observability](#monitoring--observability)
- [Auth & Identity](#auth--identity)
- [Storage & Content](#storage--content)
- [Music & Media](#music--media)

---

## AI & LLM Providers

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Anthropic API](https://docs.anthropic.com) | 70.9 | 93.5 | 48.3 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/anthropic.com/anthropic-api/2024-10-22) |
| [Groq API](https://console.groq.com/docs) | 71.6 | 93.7 | 49.5 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/groq.com/main/1.0) |
| [Amazon Bedrock Runtime](https://aws.amazon.com/bedrock/) | 70.7 | 93.7 | 47.7 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/bedrock-runtime/2023-09-30) |
| [Cohere API](https://docs.cohere.com) | 62.3 | 93.7 | 30.8 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/cohere.com/main/1.0) |
| [OpenAI API](https://platform.openai.com/docs/api-reference) | 62.3 | 76.5 | 48.2 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/openai.com/main/2.3.0) |

## Search & Recommendations

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Algolia Insights](https://www.algolia.com/doc/rest-api/insights/) | 78.0 | 93.7 | 62.3 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-insights-api/1.0.0) |
| [Algolia Recommend](https://www.algolia.com/doc/rest-api/recommend/) | 75.6 | 93.7 | 57.5 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-recommend-api/1.0.0) |
| [Algolia Ingestion](https://www.algolia.com/doc/rest-api/ingestion/) | 74.3 | 92.3 | 56.4 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-ingestion-api/1.0.0) |
| [Algolia Search](https://www.algolia.com/doc/rest-api/search/) | 71.7 | 89.5 | 54.0 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/algolia.com/algolia-search-api/1.0.0) |

## Project Management & Productivity

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [ClickUp API](https://clickup.com/api) | 74.7 | 93.7 | 55.7 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/clickup.com/clickup-api/2.0) |
| [Figma REST API](https://www.figma.com/developers/api) | 71.9 | 93.7 | 50.2 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/figma.com/figma-rest-api/1.0.0) |
| [Linear API](https://developers.linear.app) | 69.5 | 93.7 | 45.3 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/linear.app/main/1.0) |
| [Airtable Web API](https://airtable.com/developers/web/api) | 68.4 | 93.7 | 43.1 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/airtable.com/main/0.1.0) |

## Cloud Infrastructure & DevOps

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [AWS Lambda API](https://docs.aws.amazon.com/lambda/) | 74.2 | 93.7 | 54.7 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/aws-lambda-api/2015-03-31) |
| [Amazon EKS](https://docs.aws.amazon.com/eks/) | 66.3 | 93.7 | 38.9 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/eks/2017-11-01) |
| [AWS RDS Data](https://docs.aws.amazon.com/rdsdataservice/) | 66.4 | 93.7 | 39.2 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/rds-data/2018-08-01) |
| [Amazon Cognito Identity](https://docs.aws.amazon.com/cognito/) | 66.1 | 93.7 | 38.4 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/cognito-identity/2014-06-30) |
| [AWS CodeCommit](https://docs.aws.amazon.com/codecommit/) | 64.6 | 89.7 | 39.6 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/codecommit/2015-04-13) |
| [AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/) | 65.5 | 93.7 | 37.3 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/codepipeline/2015-07-09) |
| [AWS Step Functions](https://docs.aws.amazon.com/step-functions/) | 65.3 | 93.7 | 37.0 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/states/2016-11-23) |
| [Amazon CloudWatch Events](https://docs.aws.amazon.com/cloudwatch/) | 65.1 | 93.6 | 36.6 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/events/2015-10-07) |
| [AWS App Runner](https://docs.aws.amazon.com/apprunner/) | 65.2 | 93.7 | 36.6 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/apprunner/2020-05-15) |
| [AWS Lambda](https://docs.aws.amazon.com/lambda/) | 65.3 | 91.5 | 39.0 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/amazonaws.com/lambda/2015-03-31) |
| [Docker Engine API](https://docs.docker.com/engine/api/) | 65.8 | 83.2 | 48.4 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/docker.com/engine/1.33) |
| [Neon API](https://neon.tech/docs/reference/api-reference) | 62.6 | 71.9 | 53.3 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/neon.tech/main) |

## Databases & Data Platforms

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Supabase Management API](https://supabase.com/docs/reference/api) | 74.2 | 93.7 | 54.6 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/supabase.com/main) |
| [Neon API](https://neon.tech/docs/reference/api-reference) | 62.6 | 71.9 | 53.3 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/neon.tech/main) |

## Communication & Email

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [SendGrid Mail API](https://docs.sendgrid.com/api-reference) | 67.6 | 93.7 | 41.4 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/sendgrid.com/mail) |
| [Resend](https://resend.com/docs/api-reference) | 61.3 | 91.1 | 31.6 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/resend.com/main) |

## Monitoring & Observability

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Sentry API](https://docs.sentry.io/api/) | 76.4 | 93.7 | 59.1 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/sentry.io/main) |

## Auth & Identity

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Auth0 Authentication API](https://auth0.com/docs/api) | 71.3 | 93.7 | 48.9 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/auth0.com/main/2.0.0) |

## Storage & Content

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Contentful Images API](https://www.contentful.com/developers/docs/references/images-api/) | 71.2 | 93.7 | 48.7 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/contentful.com/main/1.0.0) |
| [Dropbox API v2](https://www.dropbox.com/developers/documentation) | 68.2 | 89.5 | 46.9 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/dropbox.com/dropbox-api-v2/2.0.0) |

## Music & Media

| API | Agent Effectiveness | AU | ARAX | Spec |
|-----|--------------------:|---:|-----:|------|
| [Spotify Web API](https://developer.spotify.com/documentation/web-api) | 70.8 | 87.2 | 54.4 | [View Spec](https://github.com/jentic/jentic-public-apis/tree/main/apis/openapi/spotify.com/sonallux) |

---

## Notable APIs Below the Threshold

These APIs are widely used by agents but their specs currently score below 60 on Agent Effectiveness. They work — but agents have to work harder to interpret them:

| API | Agent Effectiveness | AU | ARAX | Gap |
|-----|--------------------:|---:|-----:|-----|
| [Intercom API](https://developers.intercom.com/docs) | 60.5 | 73.9 | 47.1 | Borderline — close to threshold |
| [Stripe API](https://docs.stripe.com/api) | 45.7 | 42.6 | 48.9 | Huge spec (600+ endpoints) tanks usability |
| [Slack Web API](https://api.slack.com/methods) | 42.7 | 57.9 | 27.5 | Sparse descriptions, low semantic clarity |
| [Notion API](https://developers.notion.com) | 36.2 | 21.1 | 51.3 | Very low usability — complex nested objects |
| [GitHub REST API](https://docs.github.com/en/rest) | 30.4 | 42.6 | 18.2 | 900+ endpoints, minimal descriptions |
| [Twilio Messaging](https://www.twilio.com/docs/messaging/api) | 65.3 | 92.8 | 37.7 | Close — strong usability, weak descriptions |
| [Google Gmail API](https://developers.google.com/gmail/api) | 48.0 | 89.3 | 6.7 | High usability but almost no semantic info |
| [Shopify Admin API](https://shopify.dev/docs/api/admin-rest) | 47.2 | 42.6 | 51.8 | Large surface with limited context |

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

APIs are included based on their **Agent Effectiveness Score** (average of Agent Usability and AI-Readiness dimensions, threshold 60+). These two dimensions directly measure whether an agent can understand and operate an API from its spec alone. Scores are generated automatically by the [Jentic API Scorecard](https://github.com/jentic/jentic-api-scorecard) using the [JAIRF specification](https://github.com/jentic/api-ai-readiness-framework).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on suggesting APIs or reporting score issues.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Jentic](https://jentic.com) has waived all copyright and related rights to this work.
