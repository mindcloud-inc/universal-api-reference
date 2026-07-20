# Cloze: List Views And Audiences

Retrieves views and audiences from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-views-and-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-views-and-audiences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-views-and-audiences?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": {
        "label": {
          "plural": "string",
          "singular": "string"
        },
        "views": [
          [
            {}
          ]
        ]
      },
      "people": {
        "label": {
          "plural": "string",
          "singular": "string"
        },
        "views": [
          [
            {}
          ]
        ]
      },
      "projects": {
        "label": {
          "plural": "string",
          "singular": "string"
        },
        "views": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies` | object | View metadata for companies. |
| `companies.label` | object | Singular and plural label metadata for company views. |
| `companies.label.plural` | string | Plural label for company views. |
| `companies.label.singular` | string | Singular label for company views. |
| `companies.views[]` | array<object> | Available company views. |
| `companies.views[].id` | string | View identifier. |
| `companies.views[].name` | string | View display name. |
| `people` | object | Audience and view metadata for people. |
| `people.label` | object | Singular and plural label metadata for people views. |
| `people.label.plural` | string | Plural label for people views. |
| `people.label.singular` | string | Singular label for people views. |
| `people.views[]` | array<object> | Available people views. |
| `people.views[].id` | string | View identifier. |
| `people.views[].name` | string | View display name. |
| `projects` | object | View metadata for projects. |
| `projects.label` | object | Singular and plural label metadata for project views. |
| `projects.label.plural` | string | Plural label for project views. |
| `projects.label.singular` | string | Singular label for project views. |
| `projects.views[]` | array<object> | Available project views. |
| `projects.views[].id` | string | View identifier. |
| `projects.views[].name` | string | View display name. |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/user/views` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-views-and-audiences.md) for the provider-specific parameters and requirements.

