# Get Assignment Post with Groopit

## Endpoint

- **Method:** `GET`
- **Path:** `/Assignments(:assignmentId)/Posts(:postId)`
- **Base URL:** `https://app.groopit.co/odata`
- **Official documentation:** [Get Assignment Post](https://3996879.fs1.hubspotusercontent-na1.net/hubfs/3996879/Knowledgebase/Groopit%20OData%20Instructions%209.2024.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignmentId` | path | `string` | yes | Groopit assignment identifier. |
| `postId` | path | `string` | yes | Groopit post identifier. |
