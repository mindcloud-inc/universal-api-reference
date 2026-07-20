# <img src="https://images.mindcloud.co/apps/icons/60ec11e39eacf85d68b6e68e-favicon_1776358334961.png" alt="LionWheel Delivery logo" width="28" height="28"> LionWheel Delivery: Universal API

LionWheel Delivery lets teams create, look up, route, and manage delivery tasks through the LionWheel REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lionWheelDelivery/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lionwheel.com
- **Vendor API docs:** https://github.com/lionwheel/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Tasks by Order ID](actions/find-tasks-by-order-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lionWheelDelivery/latest/actions/find-tasks-by-order-id?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Get Visit](actions/get-visit.md) | GET | Retrieves a visit from LionWheel Delivery. |
| [Update Visit](actions/update-visit.md) | PUT | Updates an existing visit in LionWheel Delivery. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in LionWheel Delivery. |
| [Find Tasks by Order ID](actions/find-tasks-by-order-id.md) | GET | Finds tasks in LionWheel Delivery by order ID. |
| [Find Tasks by Phone](actions/find-tasks-by-phone.md) | GET | Finds tasks in LionWheel Delivery by phone number. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from LionWheel Delivery. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in LionWheel Delivery. |

