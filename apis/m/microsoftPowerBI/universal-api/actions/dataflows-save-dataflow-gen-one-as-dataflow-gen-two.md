# Microsoft Power BI: Save Dataflow Gen One As Dataflow Gen Two



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/dataflows-save-dataflow-gen-one-as-dataflow-gen-two
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/dataflows-save-dataflow-gen-one-as-dataflow-gen-two" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "gen1DataflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/dataflows-save-dataflow-gen-one-as-dataflow-gen-two', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "gen1DataflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace (group) ID of the gen1 dataflow |
| `gen1DataflowId` | string | yes | The object ID of the Gen1 dataflow to save as a native artifact |
| `description` | string | no | Optional description for the new artifact. If not provided or empty, the description from the source dataflow will be copied. Maximum length: 4000 characters |
| `displayName` | string | no | Optional display name for the new artifact. If not provided or empty, the system will generate a name based on the source dataflow name with a suffix like "\_copy1", "\_copy2", etc. to avoid naming conflicts. Maximum length: 200 characters |
| `includeSchedule` | boolean | no | Whether to include the refresh schedule from the source dataflow in the migration. If true, attempts to copy the existing schedule to the new artifact in disabled state. If false, the new artifact will be created without a schedule. |
| `targetWorkspaceId` | string | no | Optional target workspace ID where the new artifact will be created. If not provided or empty, the new artifact will be created in the same workspace as the source dataflow. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/dataflows/[:gen1DataflowId]/saveAsNativeArtifact` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dataflows-save-dataflow-gen-one-as-dataflow-gen-two.md) for the provider-specific parameters and requirements.

