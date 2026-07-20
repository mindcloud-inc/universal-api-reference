# Apollo: Bulk People Enrichment

Retrieves enriched data for up to 10 people from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-people-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-people-enrichment?connectionId=$CONNECTION_ID&details%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "details[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-people-enrichment?${params}`, {
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
| `runWaterfallEmail` | boolean | no | Set to true to enable email waterfall enrichment |
| `runWaterfallPhone` | boolean | no | Set to true to enable phone waterfall enrichment |
| `revealPersonalEmails` | boolean | no | Set to `true` if you want to enrich all matched people with personal emails. This potentially consumes credits as part of your Apollo pricing plan . The default value is `false`. If a person resides in a GDPR -compliant region, Apollo will not reveal their personal email. |
| `revealPhoneNumber` | boolean | no | Set to `true` if you want to enrich the data of all matched people with all available phone numbers, including mobile phone numbers. This potentially consumes credits as part of your Apollo pricing plan . The default value is `false`. If this parameter is set to `true`, you must enter a webhook URL for the `webhook_url` parameter. Apollo will asynchronously verify phone numbers for you, then send a JSON response that includes only details about the phone numbers to the webhook URL you provide. It can take several minutes for the phone numbers to be delivered. |
| `webhookUrl` | string | no | If you set the `reveal_phone_number` parameter to `true`, this parameter becomes mandatory. Otherwise, do not use this parameter. Enter the webhook URL that specifies where Apollo should send a JSON response that includes the phone number you requested. Apollo suggests testing this flow to ensure you receive the separate response with the phone number. If phone numbers are not revealed delivered to the webhook URL, try applying UTF-8 encoding to the webhook URL. Example: `https://webhook.site/cc4cf44e-e047-4774-8dac-473d28474e40`; `https%3A%2F%2Fwebhook.site%2Fcc4cf44e-e047-4774-8dac-473d28474e40` |
| `details[]` | array<object> | yes | Provide info for each person you want to enrich as an object within this array. Add up to 10 people. |
| `details[].firstName` | string | no | The first name of the person. This is typically used in combination with the `last_name` parameter. Example: `tim` |
| `details[].lastName` | string | no | The last name of the person. This is typically used in combination with the `first_name` parameter. Example: `zheng` |
| `details[].name` | string | no | The full name of the person. This will typically be a first name and last name separated by a space. If you use this parameter, you do not need to use the `first_name` and `last_name` parameters. Example: `tim zheng` |
| `details[].email` | string | no | The email address of the person. Example: `example@email.com` |
| `details[].hashedEmail` | string | no | The hashed email of the person. The email should adhere to either the MD5 or SHA-256 hash format. Example: `8d935115b9ff4489f2d1f9249503cadf` (MD5) or `97817c0c49994eb500ad0a5e7e2d8aed51977b26424d508f66e4e8887746a152` (SHA-256) |
| `details[].organizationName` | string | no | The name of the person's employer. This can be the current employer or a previous employer. Example: `apollo` |
| `details[].domain` | string | no | The domain name for the person's employer. This can be the current employer or a previous employer. Do not include `www.`, the `@` symbol, or similar. Example: `apollo.io` or `microsoft.com` |
| `details[].id` | string | no | The Apollo ID for the person. Each person in the Apollo database is assigned a unique ID. To find IDs, call the People API Search endpoint and identify the values for `person_id`. Example: `587cf802f65125cad923a266` |
| `details[].linkedinUrl` | string | no | The URL for the person's LinkedIn profile. Example: `http://www.linkedin.com/in/tim-zheng-677ba010` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "errorCode": {},
      "errorMessage": {},
      "matches": [
        {
          "city": "string",
          "country": "string",
          "email": "ava@example.com",
          "emailDomainCatchall": true,
          "emailStatus": {},
          "employmentHistory": [
            {
              "createdAt": {},
              "current": true,
              "degree": {},
              "description": {},
              "emails": {},
              "endDate": "2026-05-07T12:00:00.000Z",
              "gradeLevel": {},
              "id": "string",
              "key": "string",
              "kind": {},
              "major": {},
              "organizationId": "string",
              "organizationName": "Ava Chen",
              "orgMatchedByName": true,
              "rawAddress": {},
              "startDate": "2026-05-07T12:00:00.000Z",
              "title": "string",
              "updatedAt": {}
            }
          ],
          "extrapolatedEmailConfidence": {},
          "facebookUrl": {},
          "firstName": "Ava",
          "formattedAddress": "string",
          "githubUrl": {},
          "headline": "string",
          "id": "string",
          "intentStrength": {},
          "lastName": "Chen",
          "linkedinUrl": "https://example.com",
          "name": "Ava Chen",
          "organizationId": {},
          "photoUrl": "https://example.com",
          "postalCode": {},
          "revealedForCurrentTeam": true,
          "seniority": {},
          "showIntent": true,
          "state": "string",
          "streetAddress": "string",
          "timeZone": "string",
          "title": {},
          "twitterUrl": {}
        }
      ],
      "missingRecords": 1,
      "status": "string",
      "totalRequestedEnrichments": 1,
      "uniqueEnrichedRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `errorCode` | object |  |
| `errorMessage` | object |  |
| `matches[].city` | string |  |
| `matches[].country` | string |  |
| `matches[].email` | string |  |
| `matches[].emailDomainCatchall` | boolean |  |
| `matches[].emailStatus` | object |  |
| `matches[].employmentHistory[].createdAt` | object |  |
| `matches[].employmentHistory[].current` | boolean |  |
| `matches[].employmentHistory[].degree` | object |  |
| `matches[].employmentHistory[].description` | object |  |
| `matches[].employmentHistory[].emails` | object |  |
| `matches[].employmentHistory[].endDate` | date |  |
| `matches[].employmentHistory[].gradeLevel` | object |  |
| `matches[].employmentHistory[].id` | string |  |
| `matches[].employmentHistory[].key` | string |  |
| `matches[].employmentHistory[].kind` | object |  |
| `matches[].employmentHistory[].major` | object |  |
| `matches[].employmentHistory[].organizationId` | string |  |
| `matches[].employmentHistory[].organizationName` | string |  |
| `matches[].employmentHistory[].orgMatchedByName` | boolean |  |
| `matches[].employmentHistory[].rawAddress` | object |  |
| `matches[].employmentHistory[].startDate` | date |  |
| `matches[].employmentHistory[].title` | string |  |
| `matches[].employmentHistory[].updatedAt` | object |  |
| `matches[].extrapolatedEmailConfidence` | object |  |
| `matches[].facebookUrl` | object |  |
| `matches[].firstName` | string |  |
| `matches[].formattedAddress` | string |  |
| `matches[].githubUrl` | object |  |
| `matches[].headline` | string |  |
| `matches[].id` | string |  |
| `matches[].intentStrength` | object |  |
| `matches[].lastName` | string |  |
| `matches[].linkedinUrl` | string |  |
| `matches[].name` | string |  |
| `matches[].organizationId` | object |  |
| `matches[].photoUrl` | string |  |
| `matches[].postalCode` | object |  |
| `matches[].revealedForCurrentTeam` | boolean |  |
| `matches[].seniority` | object |  |
| `matches[].showIntent` | boolean |  |
| `matches[].state` | string |  |
| `matches[].streetAddress` | string |  |
| `matches[].timeZone` | string |  |
| `matches[].title` | object |  |
| `matches[].twitterUrl` | object |  |
| `missingRecords` | number |  |
| `status` | string |  |
| `totalRequestedEnrichments` | number |  |
| `uniqueEnrichedRecords` | number |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/people/bulk_match` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-people-enrichment.md) for the provider-specific parameters and requirements.

