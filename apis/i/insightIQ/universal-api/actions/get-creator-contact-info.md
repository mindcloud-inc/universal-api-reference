# InsightIQ: Get Creator Contact Info

Retrieves creator contact information from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-contact-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-contact-info?connectionId=$CONNECTION_ID&identifier=string&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "workPlatformId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-contact-info?${params}`, {
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
| `identifier` | string | yes | Identifier of the profile: username or profile URL |
| `workPlatformId` | string | yes | Work platform ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_details": {},
      "profile": {},
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_details` | object |  |
| `profile` | object |  |
| `work_platform` | object |  |

## Native endpoint

Through the native InsightIQ API, this operation is `POST /v1/social/creators/profiles/contact-info` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creator-contact-info.md) for the provider-specific parameters and requirements.

