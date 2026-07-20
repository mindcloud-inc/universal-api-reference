# Postman: Native API Reference

A consolidated summary of Postman's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://learning.postman.com/docs/developer/postman-api/intro-api
- **API base URL:** `https://api.getpostman.com`

## Authentication

### API Key

Authenticate using a Postman API key sent in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://learning.postman.com/docs/developer/postman-api/authentication)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | `POST /environments` | [docs](https://www.postman.com/postman/utility-flows/request/2g360ay/create-an-environment) |
| [Create Mock Server](actions/create-mock-server.md) | `POST /mocks` | [docs](https://www.postman.com/postman/postman-public-workspace/request/5y0q4k4/create-a-mock-server) |
| [Create Monitor](actions/create-monitor.md) | `POST /monitors` | [docs](https://www.postman.com/postman/postman-public-workspace/request/xae4ivm/create-a-monitor) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://www.postman.com/postman/utility-flows/request/bl962uv/create-a-workspace) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /environments/:environmentId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/99bqfuh/delete-an-environment) |
| [Delete Mock Server](actions/delete-mock-server.md) | `DELETE /mocks/:mockId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/qobpu42/delete-a-mock-server) |
| [Delete Monitor](actions/delete-monitor.md) | `DELETE /monitors/:monitorId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/mg98tih/delete-a-monitor) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /workspaces/:workspaceId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/ch49fs2/delete-a-workspace) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /me` | [docs](https://www.postman.com/postman/postman-public-workspace/request/ay0ymqy/get-authenticated-user) |
| [Get Environment](actions/get-environment.md) | `GET /environments/:environmentId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/rdrxdqi/get-an-environment) |
| [Get Mock Server](actions/get-mock-server.md) | `GET /mocks/:mockId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/nzbzzq9/get-a-mock-server) |
| [Get Monitor](actions/get-monitor.md) | `GET /monitors/:monitorId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/7izaj6c/get-a-monitor) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/78dkz7e/get-a-workspace) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://www.postman.com/postman/postman-public-workspace/request/bqbz8iw/get-all-environments) |
| [List Mock Server Call Logs](actions/list-mock-server-call-logs.md) | `GET /mocks/:mockId/call-logs` | [docs](https://www.postman.com/postman/postman-public-workspace/request/5a1zzxz/get-a-mock-server-s-call-logs) |
| [List Mock Servers](actions/list-mock-servers.md) | `GET /mocks` | [docs](https://www.postman.com/postman/postman-public-workspace/request/6v89u2r/get-all-mock-servers) |
| [List Monitors](actions/list-monitors.md) | `GET /monitors` | [docs](https://www.postman.com/postman/postman-public-workspace/request/fahs921/get-all-monitors) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://www.postman.com/postman/postman-public-workspace/request/mes2rzs/get-all-workspaces) |
| [Publish Mock Server](actions/publish-mock-server.md) | `POST /mocks/:mockId/publish` | [docs](https://www.postman.com/postman/postman-public-workspace/request/7mglglo/publish-a-mock-server) |
| [Run Monitor](actions/run-monitor.md) | `POST /monitors/:monitorId/run` | [docs](https://www.postman.com/postman/postman-public-workspace/request/80oupaf/run-a-monitor) |
| [Unpublish Mock Server](actions/unpublish-mock-server.md) | `DELETE /mocks/:mockId/unpublish` | [docs](https://www.postman.com/postman/postman-public-workspace/request/902qjpm/unpublish-a-mock-server) |
| [Update Environment](actions/update-environment.md) | `PATCH /environments/:environmentId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/gwlw6in/update-an-environment) |
| [Update Mock Server](actions/update-mock-server.md) | `PUT /mocks/:mockId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/ursyofi/update-a-mock-server) |
| [Update Monitor](actions/update-monitor.md) | `PUT /monitors/:monitorId` | [docs](https://www.postman.com/postman/postman-public-workspace/request/xbdpc2a/update-a-monitor) |
| [Update Workspace](actions/update-workspace.md) | `PUT /workspaces/:workspaceId` | [docs](https://www.postman.com/postman/free-public-apis/request/rkjj42d/update-a-workspace) |
