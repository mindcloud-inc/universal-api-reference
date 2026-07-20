# Pantry: Native API Reference

A consolidated summary of Pantry's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/3281832/SzmZeMLC
- **API base URL:** `https://getpantry.cloud/apiv1`

## Authentication

### Pantry ID

Connect using the Pantry ID in the request path.

### Credentials

- **Pantry ID:** `pantryId` · required · The Pantry ID used in Pantry API request paths.

[Official authentication documentation](https://documenter.getpostman.com/view/3281832/SzmZeMLC)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Replace Basket](actions/create-or-replace-basket.md) | `POST /pantry/:pantryId/basket/:basketName` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Delete Basket](actions/delete-basket.md) | `DELETE /pantry/:pantryId/basket/:basketName` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Get Basket Contents](actions/get-basket-contents.md) | `GET /pantry/:pantryId/basket/:basketName` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Get Pantry Details](actions/get-pantry-details.md) | `GET /pantry/:pantryId` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Get Public Basket Contents](actions/get-public-basket-contents.md) | `GET /public/:publicBasketId` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Get Public Basket ID](actions/get-public-basket-id.md) | `GET /pantry/:pantryId/basket/:basketName/public` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Update Basket Contents](actions/update-basket-contents.md) | `PUT /pantry/:pantryId/basket/:basketName` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
| [Update Pantry Details](actions/update-pantry-details.md) | `PUT /pantry/:pantryId` | [docs](https://documenter.getpostman.com/view/3281832/SzmZeMLC) |
