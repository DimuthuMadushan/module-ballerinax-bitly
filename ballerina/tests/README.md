# Running Tests

## Prerequisites

The tests run against a local mock of the Bitly API by default, so no credentials are needed.

To run them against the live Bitly API, set these environment variables:

| Variable | Purpose |
|---|---|
| `IS_LIVE_SERVER` | Set to `true` to call `https://api-ssl.bitly.com/v4` |
| `BITLY_ACCESS_TOKEN` | Bitly OAuth access token |
| `BITLY_GROUP_GUID` | GUID of the group to read from |
| `BITLY_ORGANIZATION_GUID` | GUID of the organization to read from |

Mutating tests are skipped when `IS_LIVE_SERVER` is `true`.

## Running the tests

```bash
./gradlew clean test
```

or, from the `ballerina` directory:

```bash
bal test
```

The suite covers link creation, update, deletion and expansion, click and country metrics, custom Bitlinks, groups, organizations, the user profile, campaigns, channels and webhooks.
