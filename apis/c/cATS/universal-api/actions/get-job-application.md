# CATS: Get Job Application

Retrieves a job application from CATS.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-job-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-job-application?connectionId=$CONNECTION_ID&applicationId=288125" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "288125"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-job-application?${params}`, {
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
| `applicationId` | number | yes | The ID of the job application to return. Example: `288125`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "Embedded": {
        "fields": [
          {
            "applicationId": 1,
            "comment": "string",
            "id": 1,
            "isRequired": true,
            "linkedCustomFieldId": {},
            "Links": {
              "self": {
                "href": "https://example.com"
              }
            },
            "minItems": {},
            "position": 1,
            "savesToField": "string",
            "size": {},
            "title": "string",
            "type": "string"
          }
        ]
      },
      "header": "string",
      "id": 1,
      "Links": {
        "fields": {
          "href": "https://example.com"
        },
        "self": {
          "href": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `Embedded.fields[].applicationId` | number |  |
| `Embedded.fields[].comment` | string |  |
| `Embedded.fields[].id` | number |  |
| `Embedded.fields[].isRequired` | boolean |  |
| `Embedded.fields[].linkedCustomFieldId` | object |  |
| `Embedded.fields[].Links.self.href` | string |  |
| `Embedded.fields[].minItems` | object |  |
| `Embedded.fields[].position` | number |  |
| `Embedded.fields[].savesToField` | string |  |
| `Embedded.fields[].size` | object |  |
| `Embedded.fields[].title` | string |  |
| `Embedded.fields[].type` | string |  |
| `header` | string |  |
| `id` | number |  |
| `Links.fields.href` | string |  |
| `Links.self.href` | string |  |

## Native endpoint

Through the native CATS API, this operation is `GET /jobs/applications/:application_id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-application.md) for the provider-specific parameters and requirements.

