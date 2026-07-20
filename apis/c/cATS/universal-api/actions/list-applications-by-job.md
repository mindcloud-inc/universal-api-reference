# CATS: List Applications By Job

Retrieves applications for a job in CATS.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-applications-by-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-applications-by-job?connectionId=$CONNECTION_ID&jobId=16789175" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "16789175"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-applications-by-job?${params}`, {
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
| `jobId` | number | yes | The ID of the job to return applications for. Example: `16789175`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "Embedded": {
        "applications": [
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
        ]
      },
      "Links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `Embedded.applications[].description` | string |  |
| `Embedded.applications[].Embedded.fields[].applicationId` | number |  |
| `Embedded.applications[].Embedded.fields[].comment` | string |  |
| `Embedded.applications[].Embedded.fields[].id` | number |  |
| `Embedded.applications[].Embedded.fields[].isRequired` | boolean |  |
| `Embedded.applications[].Embedded.fields[].linkedCustomFieldId` | object |  |
| `Embedded.applications[].Embedded.fields[].Links.self.href` | string |  |
| `Embedded.applications[].Embedded.fields[].minItems` | object |  |
| `Embedded.applications[].Embedded.fields[].position` | number |  |
| `Embedded.applications[].Embedded.fields[].savesToField` | string |  |
| `Embedded.applications[].Embedded.fields[].size` | object |  |
| `Embedded.applications[].Embedded.fields[].title` | string |  |
| `Embedded.applications[].Embedded.fields[].type` | string |  |
| `Embedded.applications[].header` | string |  |
| `Embedded.applications[].id` | number |  |
| `Embedded.applications[].Links.fields.href` | string |  |
| `Embedded.applications[].Links.self.href` | string |  |
| `Links.self.href` | string |  |
| `total` | number |  |

## Native endpoint

Through the native CATS API, this operation is `GET /jobs/:job_id/applications` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications-by-job.md) for the provider-specific parameters and requirements.

