# Weaviate Vector Store: Native API Reference

A consolidated summary of Weaviate Vector Store's API configuration and 116 documented operations, with links to official documentation.

- **Official docs:** https://docs.weaviate.io/
- **API base URL:** `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`

## Authentication

### API Key

Authenticate to a Weaviate cluster with a cluster-scoped API key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.weaviate.io/wcs/manage-clusters/authentication)

## Endpoints (116 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate a user](actions/activateuser.md) | `POST /users/db/:user_id/activate` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add Collection Property](actions/add-collection-property.md) | `POST /v1/schema/:className/properties` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add References Batch](actions/add-references-batch.md) | `POST /v1/batch/references` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add Tenants](actions/add-tenants.md) | `POST /v1/schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add permissions to a role](actions/addpermissions.md) | `POST /authz/roles/:id/add-permissions` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create a new alias](actions/aliases-create.md) | `POST /aliases` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete an alias](actions/aliases-delete.md) | `DELETE /aliases/:aliasName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List aliases](actions/aliases-get.md) | `GET /aliases` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get an alias](actions/aliases-get-alias.md) | `GET /aliases/:aliasName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update an alias](actions/aliases-update.md) | `PUT /aliases/:aliasName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Apply replication scaling plan](actions/applyreplicationscaleplan.md) | `POST /replication/scale` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Assign a role to a group](actions/assignroletogroup.md) | `POST /authz/groups/:id/assign` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Assign a role to a user](actions/assignroletouser.md) | `POST /authz/users/:id/assign` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Cancel a backup](actions/backups-cancel.md) | `DELETE /backups/:backend/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create a backup](actions/backups-create.md) | `POST /backups/:backend` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get backup creation status](actions/backups-create-status.md) | `GET /backups/:backend/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List all created backups](actions/backups-list.md) | `GET /backups/:backend` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Restore from a backup](actions/backups-restore.md) | `POST /backups/:backend/:id/restore` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Cancel a backup restoration](actions/backups-restore-cancel.md) | `DELETE /backups/:backend/:id/restore` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get backup restoration status](actions/backups-restore-status.md) | `GET /backups/:backend/:id/restore` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Cancel a replication operation](actions/cancelreplication.md) | `POST /replication/replicate/:id/cancel` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Check Cluster Live](actions/check-cluster-live.md) | `GET /v1/.well-known/live` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Check Cluster Ready](actions/check-cluster-ready.md) | `GET /v1/.well-known/ready` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get classification status](actions/classifications-get.md) | `GET /classifications/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Start a classification](actions/classifications-post.md) | `POST /classifications/` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get cluster statistics](actions/cluster-get-statistics.md) | `GET /cluster/statistics` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create Collection](actions/create-collection.md) | `POST /v1/schema` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create Object](actions/create-object.md) | `POST /v1/objects` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create Objects Batch](actions/create-objects-batch.md) | `POST /v1/batch/objects` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create new role](actions/createrole.md) | `POST /authz/roles` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create a new user](actions/createuser.md) | `POST /users/db/:user_id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Deactivate a user](actions/deactivateuser.md) | `POST /users/db/:user_id/deactivate` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /v1/schema/:className` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete Object](actions/delete-object.md) | `DELETE /v1/objects/:className/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete Objects By Filter](actions/delete-objects-by-filter.md) | `DELETE /v1/batch/objects` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete Tenants](actions/delete-tenants.md) | `DELETE /v1/schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete all replication operations](actions/deleteallreplications.md) | `DELETE /replication/replicate` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete a replication operation](actions/deletereplication.md) | `DELETE /replication/replicate/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete a role](actions/deleterole.md) | `DELETE /authz/roles/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete a user](actions/deleteuser.md) | `DELETE /users/db/:user_id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Lists all distributed tasks in the cluster](actions/distributedtasks-get.md) | `GET /tasks` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Cancel an export](actions/export-cancel.md) | `DELETE /export/:backend/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Start a new export](actions/export-create.md) | `POST /export/:backend` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get export status](actions/export-status.md) | `GET /export/:backend/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Force delete replication operations](actions/forcedeletereplications.md) | `POST /replication/replicate/force-delete` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get Cluster Meta](actions/get-cluster-meta.md) | `GET /v1/meta` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get Cluster Nodes](actions/get-cluster-nodes.md) | `GET /v1/nodes` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get Collection](actions/get-collection.md) | `GET /v1/schema/:className` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get Collection Shards](actions/get-collection-shards.md) | `GET /v1/schema/:className/shards` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get Object](actions/get-object.md) | `GET /v1/objects/:className/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get OIDC Configuration](actions/get-oidc-configuration.md) | `GET /.well-known/openid-configuration` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get sharding state](actions/getcollectionshardingstate.md) | `GET /replication/sharding-state` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List all groups of a specific type](actions/getgroups.md) | `GET /authz/groups/:groupType` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get groups that have a specific role assigned](actions/getgroupsforrole.md) | `GET /authz/roles/:id/group-assignments` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get current user info](actions/getowninfo.md) | `GET /users/own-info` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get replication scale plan](actions/getreplicationscaleplan.md) | `GET /replication/scale` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get a role](actions/getrole.md) | `GET /authz/roles/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get all roles](actions/getroles.md) | `GET /authz/roles` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get roles assigned to a specific group](actions/getrolesforgroup.md) | `GET /authz/groups/:id/roles/:groupType` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get roles assigned to a user](actions/getrolesforuser.md) | `GET /authz/users/:id/roles/:userType` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get roles assigned to a user](actions/getrolesforuserdeprecated.md) | `GET /authz/users/:id/roles` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get user info](actions/getuserinfo.md) | `GET /users/db/:user_id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get users assigned to a role](actions/getusersforrole.md) | `GET /authz/roles/:id/user-assignments` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get users assigned to a role](actions/getusersforroledeprecated.md) | `GET /authz/roles/:id/users` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Perform batched GraphQL queries](actions/graphql-batch.md) | `POST /graphql/batch` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Check whether a role possesses a permission](actions/haspermission.md) | `POST /authz/roles/:id/has-permission` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List Available Endpoints](actions/list-available-endpoints.md) | `GET /` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List Collections](actions/list-collections.md) | `GET /v1/schema` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List Objects](actions/list-objects.md) | `GET /v1/objects` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List Tenants](actions/list-tenants.md) | `GET /v1/schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List all users](actions/listallusers.md) | `GET /users/db` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [List replication operations](actions/listreplication.md) | `GET /replication/replicate/list` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Mcp.delete](actions/mcp-delete.md) | `DELETE /mcp` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Mcp.get](actions/mcp-get.md) | `GET /mcp` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Mcp.post](actions/mcp-post.md) | `POST /mcp` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get node status by collection](actions/nodes-get-class.md) | `GET /nodes/:className` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete an object](actions/objects-class-delete.md) | `DELETE /objects/:className/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get an object](actions/objects-class-get.md) | `GET /objects/:className/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Patch an object](actions/objects-class-patch.md) | `PATCH /objects/:className/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Replace an object](actions/objects-class-put.md) | `PUT /objects/:className/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add an object reference](actions/objects-class-references-create.md) | `POST /objects/:className/:id/references/:propertyName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete an object reference](actions/objects-class-references-delete.md) | `DELETE /objects/:className/:id/references/:propertyName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Replace object references](actions/objects-class-references-put.md) | `PUT /objects/:className/:id/references/:propertyName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete an object](actions/objects-delete.md) | `DELETE /objects/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get an object](actions/objects-get.md) | `GET /objects/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Patch an object](actions/objects-patch.md) | `PATCH /objects/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add an object reference](actions/objects-references-create.md) | `POST /objects/:id/references/:propertyName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete an object reference](actions/objects-references-delete.md) | `DELETE /objects/:id/references/:propertyName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Replace object references](actions/objects-references-update.md) | `PUT /objects/:id/references/:propertyName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update an object](actions/objects-update.md) | `PUT /objects/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Validate an object](actions/objects-validate.md) | `POST /objects/validate` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Remove permissions from a role](actions/removepermissions.md) | `POST /authz/roles/:id/remove-permissions` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Replace Object](actions/replace-object.md) | `PUT /v1/objects/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Initiate a replica movement](actions/replicate.md) | `POST /replication/replicate` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Retrieve a replication operation](actions/replicationdetails.md) | `GET /replication/replicate/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Revoke a role from a group](actions/revokerolefromgroup.md) | `POST /authz/groups/:id/revoke` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Revoke a role from a user](actions/revokerolefromuser.md) | `POST /authz/users/:id/revoke` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Rotate API key of a user](actions/rotateuserapikey.md) | `POST /users/db/:user_id/rotate-key` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Run GraphQL Query](actions/run-graph-ql-query.md) | `POST /v1/graphql` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete a collection (and all associated data)](actions/schema-objects-delete.md) | `DELETE /schema/:className` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get a single collection](actions/schema-objects-get.md) | `GET /schema/:className` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Add a property to a collection](actions/schema-objects-properties-add.md) | `POST /schema/:className/properties` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete a property's inverted index](actions/schema-objects-properties-delete.md) | `DELETE /schema/:className/properties/:propertyName/index/:indexName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Tokenize text using a property's configuration](actions/schema-objects-properties-tokenize.md) | `POST /schema/:className/properties/:propertyName/tokenize` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get the shards status of a collection](actions/schema-objects-shards-get.md) | `GET /schema/:className/shards` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update a shard status](actions/schema-objects-shards-update.md) | `PUT /schema/:className/shards/:shardName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update collection definition](actions/schema-objects-update.md) | `PUT /schema/:className` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete a collection's vector index.](actions/schema-objects-vectors-delete.md) | `DELETE /schema/:className/vectors/:vectorIndexName/index` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Create a new tenant](actions/tenants-create.md) | `POST /schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Delete tenants](actions/tenants-delete.md) | `DELETE /schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get the list of tenants](actions/tenants-get.md) | `GET /schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Get a specific tenant](actions/tenants-get-one.md) | `GET /schema/:className/tenants/:tenantName` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update a tenant](actions/tenants-update.md) | `PUT /schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Tokenize text](actions/tokenize.md) | `POST /tokenize` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update Object](actions/update-object.md) | `PATCH /v1/objects/:id` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
| [Update Tenants](actions/update-tenants.md) | `PUT /v1/schema/:className/tenants` | [docs](https://docs.weaviate.io/weaviate/api/rest) |
