# Polycom: Search Studio X Teams and Zoom Devices

Searches Studio X devices in Poly Lens running Teams or Zoom.

```
GET https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-studio-x-teams-and-zoom-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-studio-x-teams-and-zoom-devices?connectionId=$CONNECTION_ID&query=query%20studioXTeamsZoomDevices(%24params%3A%20DeviceFindArgs)%20%7B%20deviceSearch(params%3A%20%24params)%20%7B%20edges%20%7B%20node%20%7B%20name%20id%20connected%20serialNumber%20hardwareModel%20activeApplicationName%20activeApplicationVersion%20room%20%7B%20name%20floor%20%7D%20connections%20%7B%20name%20id%20connected%20%7D%20%7D%20%7D%20pageInfo%20%7B%20countOnPage%20totalCount%20hasNextPage%20nextToken%20%7D%20%7D%20%7D&variables.params.filter.AND%5B0%5D.OR%5B0%5D.contains=Teams&variables.params.filter.AND%5B0%5D.OR%5B1%5D.contains=Zoom&variables.params.filter.AND%5B1%5D.contains=Studio%20X&variables.params.sort.fields%5B0%5D.name=id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query studioXTeamsZoomDevices($params: DeviceFindArgs) { deviceSearch(params: $params) { edges { node { name id connected serialNumber hardwareModel activeApplicationName activeApplicationVersion room { name floor } connections { name id connected } } } pageInfo { countOnPage totalCount hasNextPage nextToken } } }",
  "variables.params.filter.AND[0].OR[0].contains": "Teams",
  "variables.params.filter.AND[0].OR[1].contains": "Zoom",
  "variables.params.filter.AND[1].contains": "Studio X",
  "variables.params.sort.fields[0].name": "id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/search-studio-x-teams-and-zoom-devices?${params}`, {
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
| `query` | string | yes | Hidden GraphQL document for the Studio X Teams-and-Zoom device search. Default: `query studioXTeamsZoomDevices($params: DeviceFindArgs) { deviceSearch(params: $params) { edges { node { name id connected serialNumber hardwareModel activeApplicationName activeApplicationVersion room { name floor } connections { name id connected } } } pageInfo { countOnPage totalCount hasNextPage nextToken } } }`. |
| `variables.params.filter.AND[0].OR[0].contains` | string | yes | First application filter value. Default: `Teams`. |
| `variables.params.filter.AND[0].OR[1].contains` | string | yes | Second application filter value. Default: `Zoom`. |
| `variables.params.filter.AND[1].contains` | string | yes | Hardware model filter value. Default: `Studio X`. |
| `variables.params.pageSize` | number | no | Maximum number of devices to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.params.sort.fields[0].name` | string | yes | Sort field name. Default: `id`. |
| `variables.params.nextToken` | string | no | Opaque token for the next page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeApplicationName": "Ava Chen",
      "activeApplicationVersion": "string",
      "connected": true,
      "connections": [
        {
          "connected": true,
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "hardwareModel": "string",
      "id": "string",
      "name": "Ava Chen",
      "room": {
        "floor": "string",
        "name": "Ava Chen"
      },
      "serialNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeApplicationName` | string |  |
| `activeApplicationVersion` | string |  |
| `connected` | boolean |  |
| `connections[].connected` | boolean |  |
| `connections[].id` | string |  |
| `connections[].name` | string |  |
| `hardwareModel` | string |  |
| `id` | string |  |
| `name` | string |  |
| `room.floor` | string |  |
| `room.name` | string |  |
| `serialNumber` | string |  |

## Native endpoint

Through the native Polycom API, this operation is `POST /graphql` (base URL `https://api.silica-prod01.io.lens.poly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-studio-x-teams-and-zoom-devices.md) for the provider-specific parameters and requirements.

