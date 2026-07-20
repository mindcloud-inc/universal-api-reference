# Affinda: Get list of all extractors

Retrieves all accessible extractors from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-extractors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-extractors?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-extractors?${params}`, {
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
| `includePublicExtractors` | string | no | Whether to include Affinda's off-the-shelf extractors. |
| `name` | string | no | Filter by name. |
| `organization` | string | yes | Filter by organization. |
| `validatable` | string | no | Filter by validatable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseExtractor": {},
      "category": "string",
      "createdDt": "2026-05-07T12:00:00.000Z",
      "fieldGroups": [
        {}
      ],
      "identifier": "string",
      "isCustom": true,
      "lastTrainedDt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "namePlural": "Ava Chen",
      "organization": {},
      "validatable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseExtractor` | object |  |
| `category` | string |  |
| `createdDt` | date |  |
| `fieldGroups` | array<object> |  |
| `identifier` | string |  |
| `isCustom` | boolean |  |
| `lastTrainedDt` | date |  |
| `name` | string |  |
| `namePlural` | string |  |
| `organization` | object |  |
| `validatable` | boolean |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/extractors` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extractors.md) for the provider-specific parameters and requirements.

