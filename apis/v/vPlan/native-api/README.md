# vPlan: Native API Reference

A consolidated summary of vPlan's API configuration and 56 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.vplan.com
- **API base URL:** `https://api.vplan.com/v1`

## Authentication

### Custom Headers

Use explicit vPlan headers without any implicit Authorization behavior.

### Credentials

- **API Key:** `apiKey` · required · vPlan API key sent as the X-Api-Key header.
- **API Env:** `apiEnv` · required · vPlan API environment identifier sent as the X-Api-Env header.

Send these headers with each API request:

```http
X-Api-Env: <apiEnv>
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.api.vplan.com/authentication-377764f0)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (56 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /activity` | [docs](https://docs.api.vplan.com/activity.md) |
| [Create Attachment Link](actions/create-attachment-link.md) | `POST /collection/[:collection_id]/attachment` | [docs](https://docs.api.vplan.com/attachment_create_link) |
| [Create Board](actions/create-board.md) | `POST /board` | [docs](https://docs.api.vplan.com/board.md) |
| [Create Card](actions/create-card.md) | `POST /collection/[:collection_id]/card` | [docs](https://docs.api.vplan.com/card.md) |
| [Create Collection](actions/create-collection.md) | `POST /collection` | [docs](https://docs.api.vplan.com/collection.md) |
| [Create Comment](actions/create-comment.md) | `POST /collection/[:collection_id]/comment` | [docs](https://docs.api.vplan.com/comment.md) |
| [Create Item](actions/create-item.md) | `POST /item` | [docs](https://docs.api.vplan.com/create-new-item-3589266e0) |
| [Create Order](actions/create-order.md) | `POST /order` | [docs](https://docs.api.vplan.com/create-new-order-3589256e0) |
| [Create Project](actions/create-project.md) | `POST /project` | [docs](https://docs.api.vplan.com/project.md) |
| [Create Relation](actions/create-relation.md) | `POST /relation` | [docs](https://docs.api.vplan.com/create-new-relation-3589276e0) |
| [Create Stage](actions/create-stage.md) | `POST /stage` | [docs](https://docs.api.vplan.com/stage.md) |
| [Create Time Tracking Entry](actions/create-time-tracking-entry.md) | `POST /time_tracking` | [docs](https://docs.api.vplan.com/create-new-timetracking-3589247e0) |
| [Create Warehouse](actions/create-warehouse.md) | `POST /warehouse` | [docs](https://docs.api.vplan.com/create-new-warehouse-3589281e0) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook` | [docs](https://docs.api.vplan.com/webhook_create) |
| [Get Activity](actions/get-activity.md) | `GET /activity/[:id]` | [docs](https://docs.api.vplan.com/activity.md) |
| [Get Attachment](actions/get-attachment.md) | `GET /collection/[:collection_id]/attachment/[:attachment_id]` | [docs](https://docs.api.vplan.com/attachment.md) |
| [Get Board](actions/get-board.md) | `GET /board/[:id]` | [docs](https://docs.api.vplan.com/board_show.md) |
| [Get Card](actions/get-card.md) | `GET /collection/[:collection_id]/card/[:card_id]` | [docs](https://docs.api.vplan.com/card.md) |
| [Get Collection](actions/get-collection.md) | `GET /collection/[:id]` | [docs](https://docs.api.vplan.com/collection.md) |
| [Get Comment](actions/get-comment.md) | `GET /collection/[:collection_id]/comment/[:comment_id]` | [docs](https://docs.api.vplan.com/comment.md) |
| [Get Group](actions/get-group.md) | `GET /group/[:id]` | [docs](https://docs.api.vplan.com/group.md) |
| [Get Item](actions/get-item.md) | `GET /item/[:id]` | [docs](https://docs.api.vplan.com/item.md) |
| [Get Order](actions/get-order.md) | `GET /order/[:id]` | [docs](https://docs.api.vplan.com/order.md) |
| [Get Project](actions/get-project.md) | `GET /project/[:id]` | [docs](https://docs.api.vplan.com/project.md) |
| [Get Relation](actions/get-relation.md) | `GET /relation/[:id]` | [docs](https://docs.api.vplan.com/relation.md) |
| [Get Resource](actions/get-resource.md) | `GET /resource/[:id]` | [docs](https://docs.api.vplan.com/resource.md) |
| [Get Stage](actions/get-stage.md) | `GET /stage/[:id]` | [docs](https://docs.api.vplan.com/stage.md) |
| [Get Time Tracking Entry](actions/get-time-tracking-entry.md) | `GET /time_tracking/[:id]` | [docs](https://docs.api.vplan.com/time_tracking.md) |
| [Get User](actions/get-user.md) | `GET /user/[:id]` | [docs](https://docs.api.vplan.com/user.md) |
| [Get Warehouse](actions/get-warehouse.md) | `GET /warehouse/[:id]` | [docs](https://docs.api.vplan.com/warehouse.md) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook/[:id]` | [docs](https://docs.api.vplan.com/webhook.md) |
| [List Activities](actions/list-activities.md) | `GET /activity` | [docs](https://docs.api.vplan.com/activity.md) |
| [List Attachments](actions/list-attachments.md) | `GET /collection/[:collection_id]/attachment` | [docs](https://docs.api.vplan.com/attachment.md) |
| [List Boards](actions/list-boards.md) | `GET /board` | [docs](https://docs.api.vplan.com/board.md) |
| [List Cards](actions/list-cards.md) | `GET /collection/[:collection_id]/card` | [docs](https://docs.api.vplan.com/card.md) |
| [List Collections](actions/list-collections.md) | `GET /collection` | [docs](https://docs.api.vplan.com/collection.md) |
| [List Comments](actions/list-comments.md) | `GET /collection/[:collection_id]/comment` | [docs](https://docs.api.vplan.com/comment.md) |
| [List Groups](actions/list-groups.md) | `GET /group` | [docs](https://docs.api.vplan.com/group.md) |
| [List Items](actions/list-items.md) | `GET /item` | [docs](https://docs.api.vplan.com/item.md) |
| [List Orders](actions/list-orders.md) | `GET /order` | [docs](https://docs.api.vplan.com/order.md) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://docs.api.vplan.com/project.md) |
| [List Relations](actions/list-relations.md) | `GET /relation` | [docs](https://docs.api.vplan.com/relation.md) |
| [List Resources](actions/list-resources.md) | `GET /resource` | [docs](https://docs.api.vplan.com/resource.md) |
| [List Stages](actions/list-stages.md) | `GET /stage` | [docs](https://docs.api.vplan.com/stage.md) |
| [List Time Tracking Entries](actions/list-time-tracking-entries.md) | `GET /time_tracking` | [docs](https://docs.api.vplan.com/time_tracking.md) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://docs.api.vplan.com/user.md) |
| [List Warehouses](actions/list-warehouses.md) | `GET /warehouse` | [docs](https://docs.api.vplan.com/warehouse.md) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook` | [docs](https://docs.api.vplan.com/webhook.md) |
| [Retrieve Authentication Details](actions/retrieve-authentication-details.md) | `GET /me` | [docs](https://docs.api.vplan.com/me.md) |
| [Update Activity](actions/update-activity.md) | `PUT /activity/[:id]` | [docs](https://docs.api.vplan.com/activity.md) |
| [Update Board](actions/update-board.md) | `PUT /board/[:id]` | [docs](https://docs.api.vplan.com/board.md) |
| [Update Card](actions/update-card.md) | `PUT /collection/[:collection_id]/card/[:card_id]` | [docs](https://docs.api.vplan.com/card.md) |
| [Update Collection](actions/update-collection.md) | `PUT /collection/[:id]` | [docs](https://docs.api.vplan.com/collection.md) |
| [Update Comment](actions/update-comment.md) | `PUT /collection/[:collection_id]/comment/[:comment_id]` | [docs](https://docs.api.vplan.com/comment.md) |
| [Update Project](actions/update-project.md) | `PUT /project/[:id]` | [docs](https://docs.api.vplan.com/project.md) |
| [Update Stage](actions/update-stage.md) | `PUT /stage/[:id]` | [docs](https://docs.api.vplan.com/stage.md) |
