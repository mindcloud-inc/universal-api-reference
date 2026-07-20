# Affinda: Get specific extractor

Retrieves a specific extractor from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-extractor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-extractor?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-extractor?${params}`, {
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
| `identifier` | string | yes | Extractor's identifier |

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

Through the native Affinda API, this operation is `GET /v3/extractors/:identifier` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extractor.md) for the provider-specific parameters and requirements.

