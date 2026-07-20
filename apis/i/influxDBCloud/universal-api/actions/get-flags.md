# InfluxDB Cloud: Get Flags

Retrieves feature flags from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-flags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-flags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-flags?${params}`, {
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
      "alertsActivity": true,
      "appMetrics": true,
      "authSessionCookieOn": true,
      "avatarWidgetMultiAccountInfo": true,
      "backendPaginatedTasks": true,
      "bulkActionDeleteTokens": true,
      "coveo": true,
      "createDeleteOrgs": true,
      "createWithFlows": true,
      "dataExplorerCsvLimit": 1,
      "deployAccordion": true,
      "enableFreeSubscriptions": true,
      "fastCsvEncoder": true,
      "fastFlows": true,
      "flowPanelRemoteCsv": true,
      "flowsCTA": true,
      "heapAnalytics": true,
      "heapanalyticsid": 1,
      "increaseCsvLimit": 1,
      "influxqlGroupcache": true,
      "influxqlQueryPlanner": "string",
      "ioxOnboarding": true,
      "logarithmicGraphScale": true,
      "measurementMultiselect": true,
      "measurementSchema": true,
      "navbarPocRequest": true,
      "navToTaskRuns": true,
      "newNotFoundPage": true,
      "newQueryBuilder": true,
      "newTimeRangeComponent": true,
      "newUsageAPI": true,
      "notebooksNewEndpoints": true,
      "onboardMQTT": true,
      "pdfImageDownload": true,
      "productComparisonPage": true,
      "quartzZuoraDisabled": true,
      "queryBuilderUseMetadataCaching": true,
      "refactorVariablesSelector": true,
      "removeExportModal": true,
      "rudderstackReporting": true,
      "saveAsScript": true,
      "schemaComposition": true,
      "sharedFlowEditing": true,
      "showAlertsInNewIOx": true,
      "showDashboardsInNewIOx": true,
      "showFnPath": true,
      "showOldDataExplorerInNewIOx": true,
      "showTasksInNewIOx": true,
      "showTemplatesInNewIOx": true,
      "showVariablesInNewIOx": true,
      "smallInsert": true,
      "subscriptionsCertificateSupport": true,
      "subscriptionsUI": true,
      "tasksUiEnhancements": true,
      "timeFilterFlags": true,
      "trackCancellations": true,
      "uiLoggingLevels": 1,
      "uiproxyd": true,
      "uiUnificationFlag": true,
      "universalLogin": true,
      "uploadCSV": true,
      "useQuartzLogin": true,
      "vwoAbTesting": true,
      "zoomRequery": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertsActivity` | boolean |  |
| `appMetrics` | boolean |  |
| `authSessionCookieOn` | boolean |  |
| `avatarWidgetMultiAccountInfo` | boolean |  |
| `backendPaginatedTasks` | boolean |  |
| `bulkActionDeleteTokens` | boolean |  |
| `coveo` | boolean |  |
| `createDeleteOrgs` | boolean |  |
| `createWithFlows` | boolean |  |
| `dataExplorerCsvLimit` | number |  |
| `deployAccordion` | boolean |  |
| `enableFreeSubscriptions` | boolean |  |
| `fastCsvEncoder` | boolean |  |
| `fastFlows` | boolean |  |
| `flowPanelRemoteCsv` | boolean |  |
| `flowsCTA` | boolean |  |
| `heapAnalytics` | boolean |  |
| `heapanalyticsid` | number |  |
| `increaseCsvLimit` | number |  |
| `influxqlGroupcache` | boolean |  |
| `influxqlQueryPlanner` | string |  |
| `ioxOnboarding` | boolean |  |
| `logarithmicGraphScale` | boolean |  |
| `measurementMultiselect` | boolean |  |
| `measurementSchema` | boolean |  |
| `navbarPocRequest` | boolean |  |
| `navToTaskRuns` | boolean |  |
| `newNotFoundPage` | boolean |  |
| `newQueryBuilder` | boolean |  |
| `newTimeRangeComponent` | boolean |  |
| `newUsageAPI` | boolean |  |
| `notebooksNewEndpoints` | boolean |  |
| `onboardMQTT` | boolean |  |
| `pdfImageDownload` | boolean |  |
| `productComparisonPage` | boolean |  |
| `quartzZuoraDisabled` | boolean |  |
| `queryBuilderUseMetadataCaching` | boolean |  |
| `refactorVariablesSelector` | boolean |  |
| `removeExportModal` | boolean |  |
| `rudderstackReporting` | boolean |  |
| `saveAsScript` | boolean |  |
| `schemaComposition` | boolean |  |
| `sharedFlowEditing` | boolean |  |
| `showAlertsInNewIOx` | boolean |  |
| `showDashboardsInNewIOx` | boolean |  |
| `showFnPath` | boolean |  |
| `showOldDataExplorerInNewIOx` | boolean |  |
| `showTasksInNewIOx` | boolean |  |
| `showTemplatesInNewIOx` | boolean |  |
| `showVariablesInNewIOx` | boolean |  |
| `smallInsert` | boolean |  |
| `subscriptionsCertificateSupport` | boolean |  |
| `subscriptionsUI` | boolean |  |
| `tasksUiEnhancements` | boolean |  |
| `timeFilterFlags` | boolean |  |
| `trackCancellations` | boolean |  |
| `uiLoggingLevels` | number |  |
| `uiproxyd` | boolean |  |
| `uiUnificationFlag` | boolean |  |
| `universalLogin` | boolean |  |
| `uploadCSV` | boolean |  |
| `useQuartzLogin` | boolean |  |
| `vwoAbTesting` | boolean |  |
| `zoomRequery` | boolean |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /flags` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flags.md) for the provider-specific parameters and requirements.

