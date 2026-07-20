# RocketReach: Lookup Universal Person

Retrieves a person from RocketReach Universal lookup.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-universal-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-universal-person?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-universal-person?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentEmployer` | string | no | Current employer of the desired profile. Must be specified along with Name. Example: `RocketReach`. |
| `email` | string | no | An email address for the desired profile. Example: `jamie@rocketreach.co`. |
| `id` | number | no | RocketReach internal unique profile ID. Example: `123456`. |
| `linkedinUrl` | string | no | LinkedIn URL of the desired profile. Example: `www.linkedin.com/in/jamesgullbrand`. |
| `name` | string | no | Name of the desired profile. Must be specified along with Current Employer. Example: `Jamie Gullbrand`. |
| `npiNumber` | number | no | An NPI number for the desired profile, for US healthcare professionals. Example: `1234567890`. |
| `title` | string | no | Job title of the desired profile. Example: `Product Manager`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkedinExtUrl` | string | no | Deprecated: use LinkedIn URL. Example: `www.linkedin.com/in/jamesgullbrand`. |
| `webhookId` | number | no | Webhook ID to receive lookup results. Example: `12345`. |
| `returnCachedEmails` | boolean | no | Whether cached emails can be included while the lookup is still in progress. Default: `true`. |
| `revealDetailedPersonEnrichment` | boolean | no | Whether to reveal detailed person enrichment data. Default: `false`. |
| `revealHealthcareEnrichment` | boolean | no | Whether to reveal healthcare enrichment data. Default: `false`. |
| `revealPersonalEmail` | boolean | no | Whether to reveal personal email enrichment data. Default: `false`. |
| `revealPhone` | boolean | no | Whether to reveal phone enrichment data. Default: `false`. |
| `revealProfessionalEmail` | boolean | no | Whether to reveal professional email enrichment data. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RocketReach API returns.

## Native endpoint

Through the native RocketReach API, this operation is `GET /universal/person/lookup` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-universal-person.md) for the provider-specific parameters and requirements.

