# Apollo: People Enrichment

Retrieves enriched data for a person from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/people-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/people-enrichment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/people-enrichment?${params}`, {
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
| `firstName` | string | no | The first name of the person. This is typically used in combination with the `last_name` parameter. Example: `tim` |
| `lastName` | string | no | The last name of the person. This is typically used in combination with the `first_name` parameter. Example: `zheng` |
| `name` | string | no | The full name of the person. This will typically be a first name and last name separated by a space. If you use this parameter, you do not need to use the `first_name` and `last_name` parameters. Example: `tim zheng` |
| `email` | string | no | The email address of the person. Example: `example@email.com` |
| `hashedEmail` | string | no | The hashed email of the person. The email should adhere to either the MD5 or SHA-256 hash format. Example: `8d935115b9ff4489f2d1f9249503cadf` (MD5) or `97817c0c49994eb500ad0a5e7e2d8aed51977b26424d508f66e4e8887746a152` (SHA-256) |
| `organizationName` | string | no | The name of the person's employer. This can be the current employer or a previous employer. Example: `apollo` |
| `domain` | string | no | The domain name for the person's employer. This can be the current employer or a previous employer. Do not include `www.`, the `@` symbol, or similar. Example: `apollo.io` or `microsoft.com` |
| `id` | string | no | The Apollo ID for the person. Each person in the Apollo database is assigned a unique ID. To find IDs, call the People API Search endpoint and identify the values for `person_id`. Example: `587cf802f65125cad923a266` |
| `linkedin_url` | string | no | The URL for the person's LinkedIn profile. Example: http://www.linkedin.com/in/tim-zheng-677ba010 |
| `linkedinUrl` | string | no | The URL for the person's LinkedIn profile. Example: `http://www.linkedin.com/in/tim-zheng-677ba010` |
| `reveal_personal_emails` | boolean | no | Set to true if you want to enrich the person's data with personal emails. This potentially consumes credits as part of your Apollo pricing plan. The default value is false. If a person resides in a GDPR-compliant region, Apollo will not reveal their personal email. Default: `false`. |
| `runWaterfallEmail` | boolean | no | Set to true to enable email waterfall enrichment |
| `retrievePhoneNumber` | boolean | no | Set to true if you want to enrich the person's data with all available phone numbers, including mobile phone numbers. This potentially consumes credits as part of your Apollo pricing plan. The default value is false. If this parameter is set to true, you must enter a webhook URL for the webhook_url parameter. Apollo will asynchronously verify phone numbers for you, then send a JSON response that includes only details about the person's phone numbers to the webhook URL you provide. It can take several minutes for the phone numbers to be delivered. Default: `false`. |
| `runWaterfallPhone` | boolean | no | Set to true to enable phone waterfall enrichment |
| `revealPersonalEmails` | boolean | no | Set to `true` if you want to enrich the person's data with personal emails. This potentially consumes credits as part of your Apollo pricing plan . The default value is `false`. If a person resides in a GDPR -compliant region, Apollo will not reveal their personal email. |
| `revealPhoneNumber` | boolean | no | Set to `true` if you want to enrich the person's data with all available phone numbers, including mobile phone numbers. This potentially consumes credits as part of your Apollo pricing plan . The default value is `false`. If this parameter is set to `true`, you must enter a webhook URL for the `webhook_url` parameter. Apollo will asynchronously verify phone numbers for you, then send a JSON response that includes only details about the person's phone numbers to the webhook URL you provide. It can take several minutes for the phone numbers to be delivered. |
| `webhookUrl` | string | no | If you set the `reveal_phone_number` parameter to `true`, this parameter becomes mandatory. Otherwise, do not use this parameter. Enter the webhook URL that specifies where Apollo should send a JSON response that includes the phone number you requested. Apollo suggests testing this flow to ensure you receive the separate response with the phone number. If phone numbers are not revealed delivered to the webhook URL, try applying UTF-8 encoding to the webhook URL. Example: `https://webhook.site/cc4cf44e-e047-4774-8dac-473d28474e40`; `https%3A%2F%2Fwebhook.site%2Fcc4cf44e-e047-4774-8dac-473d28474e40` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": {},
      "emailDomainCatchall": true,
      "emailStatus": {},
      "extrapolatedEmailConfidence": {},
      "facebookUrl": {},
      "firstName": {},
      "githubUrl": {},
      "headline": {},
      "id": "string",
      "intentStrength": {},
      "lastName": {},
      "linkedinUrl": {},
      "name": "Ava Chen",
      "organizationId": {},
      "photoUrl": {},
      "revealedForCurrentTeam": true,
      "seniority": {},
      "showIntent": true,
      "title": {},
      "twitterUrl": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | object |  |
| `emailDomainCatchall` | boolean |  |
| `emailStatus` | object |  |
| `extrapolatedEmailConfidence` | object |  |
| `facebookUrl` | object |  |
| `firstName` | object |  |
| `githubUrl` | object |  |
| `headline` | object |  |
| `id` | string |  |
| `intentStrength` | object |  |
| `lastName` | object |  |
| `linkedinUrl` | object |  |
| `name` | string |  |
| `organizationId` | object |  |
| `photoUrl` | object |  |
| `revealedForCurrentTeam` | boolean |  |
| `seniority` | object |  |
| `showIntent` | boolean |  |
| `title` | object |  |
| `twitterUrl` | object |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/people/match` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/people-enrichment.md) for the provider-specific parameters and requirements.

