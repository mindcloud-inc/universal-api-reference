# DataForB2B: Enrich Profile

Retrieves enriched profile data from DataForB2B.

```
GET https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/enrich-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/enrich-profile?connectionId=$CONNECTION_ID&profileIdentifier=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fsatyanadella%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileIdentifier": "https://www.linkedin.com/in/satyanadella/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/enrich-profile?${params}`, {
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
| `profileIdentifier` | string | yes | Profile URL or profile ID to enrich. Default: `https://www.linkedin.com/in/satyanadella/`. |
| `enrichProfile` | boolean | no | Whether to fetch the full profile object. Default: `true`. |
| `enrichWorkEmail` | boolean | no | Whether to enrich the work email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "personal_email": {},
      "phone": {},
      "profile": {},
      "work_email": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `personal_email` | object |  |
| `phone` | object |  |
| `profile` | object |  |
| `work_email` | object |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /enrich/profile` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-profile.md) for the provider-specific parameters and requirements.

