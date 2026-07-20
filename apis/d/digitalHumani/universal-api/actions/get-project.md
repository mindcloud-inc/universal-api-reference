# Digital Humani: Get Project

Retrieves a reforestation project from Digital Humani by ID.

```
GET https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | The Digital Humani project ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "location_en": "string",
      "name": "Ava Chen",
      "reforestationCompanyAddress_en": "string",
      "reforestationCompanyAddress_fr": "string",
      "reforestationCompanyName_en": "Ava Chen",
      "reforestationCompanyName_fr": "Ava Chen",
      "reforestationCompanyWebsite_en": "string",
      "reforestationCompanyWebsite_fr": "string",
      "reforestationProjectCountry_en": "string",
      "reforestationProjectCountry_fr": "string",
      "reforestationProjectDescription_en": "string",
      "reforestationProjectDescription_fr": "string",
      "reforestationProjectImageURL_en": "https://example.com",
      "reforestationProjectImageURL_fr": "https://example.com",
      "reforestationProjectWebsite_en": "string",
      "reforestationProjectWebsite_fr": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | date |  |
| `id` | string |  |
| `location_en` | string |  |
| `name` | string |  |
| `reforestationCompanyAddress_en` | string |  |
| `reforestationCompanyAddress_fr` | string |  |
| `reforestationCompanyName_en` | string |  |
| `reforestationCompanyName_fr` | string |  |
| `reforestationCompanyWebsite_en` | string |  |
| `reforestationCompanyWebsite_fr` | string |  |
| `reforestationProjectCountry_en` | string |  |
| `reforestationProjectCountry_fr` | string |  |
| `reforestationProjectDescription_en` | string |  |
| `reforestationProjectDescription_fr` | string |  |
| `reforestationProjectImageURL_en` | string |  |
| `reforestationProjectImageURL_fr` | string |  |
| `reforestationProjectWebsite_en` | string |  |
| `reforestationProjectWebsite_fr` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Digital Humani API, this operation is `GET /project/:id` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

