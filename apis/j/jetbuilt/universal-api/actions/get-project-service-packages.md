# Jetbuilt: Get Project Service Packages

Retrieve all of the service_packages attached to a given project.

```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-service-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-service-packages?connectionId=$CONNECTION_ID&projectID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-service-packages?${params}`, {
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
| `projectID` | string | yes |  |
| `servicePackageID` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jetbuilt API returns.

## Native endpoint

Through the native Jetbuilt API, this operation is `GET projects/:projectID/service_packages/[:servicePackageID]` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-service-packages.md) for the provider-specific parameters and requirements.

