# Routee: Track multiple Number Lookup requests with filters

Tracks multiple number lookup requests with filters in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-number-lookup-requests-with-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-number-lookup-requests-with-filters?connectionId=$CONNECTION_ID&fieldName=Ava%20Chen&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldName": "Ava Chen",
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-multiple-number-lookup-requests-with-filters?${params}`, {
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
| `dateStart` | date | no | ISO-8601 date-time format |
| `dateEnd` | date | no | ISO-8601 date-time format |
| `page` | number | no | The page number to retrieve, default value is 0 (meaning the first page) |
| `size` | number | no | The number of items to retrieve, default value is 10. |
| `sort` | string | no | The field name that will be used to sort the results. |
| `fieldName` | string | yes | The name of the field to filter. Possible values: 'lookupID', 'network', 'label', 'country', 'status', 'ported', 'imsi', 'roaming', 'groups', 'campaignName', 'campaignID'. If a non-existed field name value is used then all the results are returned. |
| `searchTerm` | string | yes | The exact value that the specified field must match. |
| `searchOperator` | string | no | Optional: The operator upon which the search operation will be executed. Possible values: 'is', 'is_not', 'contains', 'starts_with', 'ends_with'. If missing defaults to 'is'. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": "string",
      "last": "string",
      "number": "string",
      "numberOfElements": "string",
      "size": "string",
      "totalElements": "string",
      "totalPages": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].applicationName` | string |  |
| `content[].createdAt` | string |  |
| `content[].details` | object |  |
| `content[].details.country` | object |  |
| `content[].details.country.code` | string |  |
| `content[].details.country.isoA3Code` | string |  |
| `content[].details.country.localeName` | string |  |
| `content[].details.country.name` | string |  |
| `content[].details.imsi` | string |  |
| `content[].details.mcc` | string |  |
| `content[].details.network` | object |  |
| `content[].details.network.mnc` | string |  |
| `content[].details.network.name` | string |  |
| `content[].details.ported` | boolean |  |
| `content[].details.portedNetwork` | object |  |
| `content[].details.portedNetwork.mnc` | string |  |
| `content[].details.portedNetwork.name` | string |  |
| `content[].details.roamingNetwork` | object |  |
| `content[].details.roamingNetwork.country` | string |  |
| `content[].details.roamingNetwork.countryIsoCode` | string |  |
| `content[].details.roamingNetwork.mmc` | string |  |
| `content[].details.roamingNetwork.mnc` | string |  |
| `content[].details.roamingNetwork.network` | string |  |
| `content[].details.roamingNetwork.state` | string |  |
| `content[].label` | string |  |
| `content[].lookupId` | string |  |
| `content[].statusInfo` | object |  |
| `content[].statusInfo.description` | string |  |
| `content[].statusInfo.status` | string |  |
| `content[].statusInfo.updatedAt` | string |  |
| `content[].to` | string |  |
| `first` | string |  |
| `last` | string |  |
| `number` | string |  |
| `numberOfElements` | string |  |
| `size` | string |  |
| `totalElements` | string |  |
| `totalPages` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /lookup/tracking` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-multiple-number-lookup-requests-with-filters.md) for the provider-specific parameters and requirements.

