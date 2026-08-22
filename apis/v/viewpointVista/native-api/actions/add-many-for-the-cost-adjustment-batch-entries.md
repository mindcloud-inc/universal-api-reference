# Add Many for the Cost Adjustment Batch Entries with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/jc/2/data/cost_adj_bat_entries/actions/add_many`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Many for the Cost Adjustment Batch Entries](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datacost_adj_bat_entriesactionsadd_many)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postCacheChanges` | body | `boolean` | no | provide true to have the action posting any cache updates as part of the action processing. False if omitted |
| `items[]` | body | `array` | yes | array of objects |
