# <img src="https://images.mindcloud.co/apps/icons/pixela_1777903311739.png" alt="Pixela logo" width="28" height="28"> Pixela: Universal API

Pixela is a pixel-based habit and activity tracking API for creating GitHub-like contribution graphs and recording daily quantities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pixela/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pixe.la/
- **Vendor API docs:** https://docs.pixe.la/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Graphs](actions/list-graphs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-graphs?connectionId=$CONNECTION_ID&username=a-know" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Graph

| Action | Method | Description |
| --- | --- | --- |
| [Create Graph](actions/create-graph.md) | POST | Creates a new graph definition in Pixela. |
| [Delete Graph](actions/delete-graph.md) | DELETE | Deletes an existing graph definition from Pixela. |
| [Get Graph Definition](actions/get-graph-definition.md) | GET | Retrieves a graph definition from Pixela. |
| [List Graphs](actions/list-graphs.md) | GET | Retrieves all graph definitions in Pixela. |
| [Update Graph](actions/update-graph.md) | PUT | Updates an existing graph definition in Pixela. |

### Graph Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Graph Stats](actions/get-graph-stats.md) | GET | Retrieves statistics for a Pixela graph. |

### Graph Svg

| Action | Method | Description |
| --- | --- | --- |
| [Get Graph SVG](actions/get-graph-svg.md) | GET | Retrieves a Pixela graph as an SVG diagram. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Add To Pixel](actions/add-to-pixel.md) | PUT | Adds quantity to today's Pixela pixel using the graph timezone. |
| [Add To Specific Pixel](actions/add-to-specific-pixel.md) | PUT | Adds quantity to a specific Pixela pixel by date. |
| [Create Multiple Pixels](actions/create-multiple-pixels.md) | POST | Creates multiple pixels in a Pixela graph. |
| [Create Pixel](actions/create-pixel.md) | POST | Creates a new pixel in a Pixela graph. |
| [Decrement Pixel](actions/decrement-pixel.md) | PUT | Decrements today's pixel in Pixela using the graph timezone. |
| [Delete Pixel](actions/delete-pixel.md) | DELETE | Deletes an existing pixel from a Pixela graph. |
| [Get Latest Pixel](actions/get-latest-pixel.md) | GET | Retrieves the latest pixel from a Pixela graph. |
| [Get Pixel](actions/get-pixel.md) | GET | Retrieves a pixel from a Pixela graph by date. |
| [Get Today's Pixel](actions/get-todays-pixel.md) | GET | Retrieves today's pixel from a Pixela graph. |
| [Increment Pixel](actions/increment-pixel.md) | PUT | Increments today's pixel in Pixela using the graph timezone. |
| [List Graph Pixels](actions/list-graph-pixels.md) | GET | Retrieves pixels from a Pixela graph by date range. |
| [Subtract From Pixel](actions/subtract-from-pixel.md) | PUT | Subtracts quantity from today's Pixela pixel using the graph timezone. |
| [Subtract From Specific Pixel](actions/subtract-from-specific-pixel.md) | PUT | Subtracts quantity from a specific Pixela pixel by date. |
| [Update Pixel](actions/update-pixel.md) | PUT | Updates a pixel in Pixela, or creates it if missing. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Pixela. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Pixela. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhook definitions from Pixela. |

