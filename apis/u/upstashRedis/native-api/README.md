# Upstash Redis: Native API Reference

A consolidated summary of Upstash Redis's API configuration and 257 documented operations, with links to official documentation.

- **Official docs:** https://upstash.com/docs/redis/features/restapi
- **API base URL:** `https://choice-oriole-98954.upstash.io`

## Authentication

### API Key

Use the Upstash standard REST token. MindCloud injects it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://upstash.com/docs/redis/features/restapi)

## Endpoints (257 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [ACL](actions/acl.md) | `GET /acl` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [APPEND](actions/append.md) | `GET /append` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [AUTH](actions/auth.md) | `GET /auth` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BITCOUNT](actions/bitcount.md) | `GET /bitcount` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BITFIELD](actions/bitfield.md) | `GET /bitfield` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BITFIELD_RO](actions/bitfield-ro.md) | `GET /bitfield_ro` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BITOP](actions/bitop.md) | `GET /bitop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BITPOS](actions/bitpos.md) | `GET /bitpos` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BLMOVE](actions/blmove.md) | `GET /blmove` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BLMPOP](actions/blmpop.md) | `GET /blmpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BLPOP](actions/blpop.md) | `GET /blpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BRPOP](actions/brpop.md) | `GET /brpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BRPOPLPUSH](actions/brpoplpush.md) | `GET /brpoplpush` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BZMPOP](actions/bzmpop.md) | `GET /bzmpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BZPOPMAX](actions/bzpopmax.md) | `GET /bzpopmax` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [BZPOPMIN](actions/bzpopmin.md) | `GET /bzpopmin` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [Check Key Exists](actions/check-key-exists.md) | `GET /exists/:key` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [CLIENT GETNAME](actions/client-getname.md) | `GET /client/getname` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [CLIENT ID](actions/client-id.md) | `GET /client/id` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [CLIENT INFO](actions/client-info.md) | `GET /client/info` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [CLIENT LIST](actions/client-list.md) | `GET /client/list` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [CLIENT SETINFO](actions/client-setinfo.md) | `GET /client/setinfo` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [CLIENT SETNAME](actions/client-setname.md) | `GET /client/setname` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [COPY](actions/copy.md) | `GET /copy` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [DBSIZE](actions/dbsize.md) | `GET /dbsize` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [DECR](actions/decr.md) | `GET /decr` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [DECRBY](actions/decrby.md) | `GET /decrby` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [DEL](actions/del.md) | `GET /del` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [Delete Key](actions/delete-key.md) | `GET /del/:key` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [DISCARD](actions/discard.md) | `GET /discard` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [DUMP](actions/dump.md) | `GET /dump` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ECHO](actions/echo.md) | `GET /echo` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EVAL](actions/eval.md) | `GET /eval` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EVAL_RO](actions/eval-ro.md) | `GET /eval_ro` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EVALSHA](actions/evalsha.md) | `GET /evalsha` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EVALSHA_RO](actions/evalsha-ro.md) | `GET /evalsha_ro` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EXEC](actions/exec.md) | `GET /exec` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EXISTS](actions/exists.md) | `GET /exists` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EXPIRE](actions/expire.md) | `GET /expire` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EXPIREAT](actions/expireat.md) | `GET /expireat` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [EXPIRETIME](actions/expiretime.md) | `GET /expiretime` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FCALL](actions/fcall.md) | `GET /fcall` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FCALL_RO](actions/fcall-ro.md) | `GET /fcall_ro` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FLUSHALL](actions/flushall.md) | `GET /flushall` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FLUSHDB](actions/flushdb.md) | `GET /flushdb` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FUNCTION DELETE](actions/function-delete.md) | `GET /function/delete` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FUNCTION FLUSH](actions/function-flush.md) | `GET /function/flush` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FUNCTION KILL](actions/function-kill.md) | `GET /function/kill` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FUNCTION LIST](actions/function-list.md) | `GET /function/list` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FUNCTION LOAD](actions/function-load.md) | `GET /function/load` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [FUNCTION STATS](actions/function-stats.md) | `GET /function/stats` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEOADD](actions/geoadd.md) | `GET /geoadd` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEODIST](actions/geodist.md) | `GET /geodist` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEOHASH](actions/geohash.md) | `GET /geohash` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEOPOS](actions/geopos.md) | `GET /geopos` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEORADIUS](actions/georadius.md) | `GET /georadius` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEORADIUS_RO](actions/georadius-ro.md) | `GET /georadius_ro` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEORADIUSBYMEMBER](actions/georadiusbymember.md) | `GET /georadiusbymember` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEORADIUSBYMEMBER_RO](actions/georadiusbymember-ro.md) | `GET /georadiusbymember_ro` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEOSEARCH](actions/geosearch.md) | `GET /geosearch` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GEOSEARCHSTORE](actions/geosearchstore.md) | `GET /geosearchstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GET](actions/get.md) | `GET /get` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [Get Database Info](actions/get-database-info.md) | `GET /info` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [Get Key TTL](actions/get-key-ttl.md) | `GET /ttl/:key` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [Get Key Value](actions/get-key-value.md) | `GET /get/:key` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [GETBIT](actions/getbit.md) | `GET /getbit` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GETDEL](actions/getdel.md) | `GET /getdel` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GETEX](actions/getex.md) | `GET /getex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GETRANGE](actions/getrange.md) | `GET /getrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [GETSET](actions/getset.md) | `GET /getset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HDEL](actions/hdel.md) | `GET /hdel` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HELLO](actions/hello.md) | `GET /hello` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HEXISTS](actions/hexists.md) | `GET /hexists` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HEXPIRE](actions/hexpire.md) | `GET /hexpire` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HEXPIREAT](actions/hexpireat.md) | `GET /hexpireat` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HEXPIRETIME](actions/hexpiretime.md) | `GET /hexpiretime` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HGET](actions/hget.md) | `GET /hget` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HGETALL](actions/hgetall.md) | `GET /hgetall` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HGETDEL](actions/hgetdel.md) | `GET /hgetdel` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HGETEX](actions/hgetex.md) | `GET /hgetex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HINCRBY](actions/hincrby.md) | `GET /hincrby` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HINCRBYFLOAT](actions/hincrbyfloat.md) | `GET /hincrbyfloat` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HKEYS](actions/hkeys.md) | `GET /hkeys` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HLEN](actions/hlen.md) | `GET /hlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HMGET](actions/hmget.md) | `GET /hmget` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HMSET](actions/hmset.md) | `GET /hmset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HPERSIST](actions/hpersist.md) | `GET /hpersist` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HPEXPIRE](actions/hpexpire.md) | `GET /hpexpire` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HPEXPIREAT](actions/hpexpireat.md) | `GET /hpexpireat` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HPEXPIRETIME](actions/hpexpiretime.md) | `GET /hpexpiretime` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HPTTL](actions/hpttl.md) | `GET /hpttl` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HRANDFIELD](actions/hrandfield.md) | `GET /hrandfield` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HSCAN](actions/hscan.md) | `GET /hscan` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HSET](actions/hset.md) | `GET /hset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HSETEX](actions/hsetex.md) | `GET /hsetex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HSETNX](actions/hsetnx.md) | `GET /hsetnx` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HSTRLEN](actions/hstrlen.md) | `GET /hstrlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HTTL](actions/httl.md) | `GET /httl` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [HVALS](actions/hvals.md) | `GET /hvals` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [INCR](actions/incr.md) | `GET /incr` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [INCRBY](actions/incrby.md) | `GET /incrby` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [INCRBYFLOAT](actions/incrbyfloat.md) | `GET /incrbyfloat` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.ARRAPPEND](actions/json-arrappend.md) | `GET /json.arrappend` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.ARRINDEX](actions/json-arrindex.md) | `GET /json.arrindex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.ARRINSERT](actions/json-arrinsert.md) | `GET /json.arrinsert` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.ARRLEN](actions/json-arrlen.md) | `GET /json.arrlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.ARRPOP](actions/json-arrpop.md) | `GET /json.arrpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.ARRTRIM](actions/json-arrtrim.md) | `GET /json.arrtrim` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.CLEAR](actions/json-clear.md) | `GET /json.clear` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.DEL](actions/json-del.md) | `GET /json.del` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.FORGET](actions/json-forget.md) | `GET /json.forget` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.GET](actions/json-get.md) | `GET /json.get` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.MERGE](actions/json-merge.md) | `GET /json.merge` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.MGET](actions/json-mget.md) | `GET /json.mget` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.MSET](actions/json-mset.md) | `GET /json.mset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.NUMINCRBY](actions/json-numincrby.md) | `GET /json.numincrby` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.NUMMULTBY](actions/json-nummultby.md) | `GET /json.nummultby` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.OBJKEYS](actions/json-objkeys.md) | `GET /json.objkeys` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.OBJLEN](actions/json-objlen.md) | `GET /json.objlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.RESP](actions/json-resp.md) | `GET /json.resp` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.SET](actions/json-set.md) | `GET /json.set` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.STRAPPEND](actions/json-strappend.md) | `GET /json.strappend` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.STRLEN](actions/json-strlen.md) | `GET /json.strlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.TOGGLE](actions/json-toggle.md) | `GET /json.toggle` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [JSON.TYPE](actions/json-type.md) | `GET /json.type` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [KEYS](actions/keys.md) | `GET /keys` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LINDEX](actions/lindex.md) | `GET /lindex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LINSERT](actions/linsert.md) | `GET /linsert` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LLEN](actions/llen.md) | `GET /llen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LMOVE](actions/lmove.md) | `GET /lmove` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LMPOP](actions/lmpop.md) | `GET /lmpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LPOP](actions/lpop.md) | `GET /lpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LPOS](actions/lpos.md) | `GET /lpos` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LPUSH](actions/lpush.md) | `GET /lpush` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LPUSHX](actions/lpushx.md) | `GET /lpushx` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LRANGE](actions/lrange.md) | `GET /lrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LREM](actions/lrem.md) | `GET /lrem` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LSET](actions/lset.md) | `GET /lset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [LTRIM](actions/ltrim.md) | `GET /ltrim` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [MGET](actions/mget.md) | `GET /mget` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [MONITOR](actions/monitor.md) | `GET /monitor` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [MSET](actions/mset.md) | `GET /mset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [MSETNX](actions/msetnx.md) | `GET /msetnx` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [MULTI](actions/multi.md) | `GET /multi` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PERSIST](actions/persist.md) | `GET /persist` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PEXPIRE](actions/pexpire.md) | `GET /pexpire` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PEXPIREAT](actions/pexpireat.md) | `GET /pexpireat` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PEXPIRETIME](actions/pexpiretime.md) | `GET /pexpiretime` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PFADD](actions/pfadd.md) | `GET /pfadd` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PFCOUNT](actions/pfcount.md) | `GET /pfcount` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PFMERGE](actions/pfmerge.md) | `GET /pfmerge` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [Ping](actions/ping.md) | `GET /ping` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [PSETEX](actions/psetex.md) | `GET /psetex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PSUBSCRIBE](actions/psubscribe.md) | `GET /psubscribe` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PTTL](actions/pttl.md) | `GET /pttl` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PUBLISH](actions/publish.md) | `GET /publish` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [Publish Message](actions/publish-message.md) | `POST /publish/:channel/:message` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [PUBSUB](actions/pubsub.md) | `GET /pubsub` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [PUNSUBSCRIBE](actions/punsubscribe.md) | `GET /punsubscribe` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [QUIT](actions/quit.md) | `GET /quit` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RANDOMKEY](actions/randomkey.md) | `GET /randomkey` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RENAME](actions/rename.md) | `GET /rename` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RENAMENX](actions/renamenx.md) | `GET /renamenx` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RESET](actions/reset.md) | `GET /reset` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RESTORE](actions/restore.md) | `GET /restore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RPOP](actions/rpop.md) | `GET /rpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RPOPLPUSH](actions/rpoplpush.md) | `GET /rpoplpush` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RPUSH](actions/rpush.md) | `GET /rpush` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [RPUSHX](actions/rpushx.md) | `GET /rpushx` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SADD](actions/sadd.md) | `GET /sadd` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SCAN](actions/scan.md) | `GET /scan` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SCARD](actions/scard.md) | `GET /scard` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SCRIPT EXISTS](actions/script-exists.md) | `GET /script/exists` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SCRIPT FLUSH](actions/script-flush.md) | `GET /script/flush` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SCRIPT LOAD](actions/script-load.md) | `GET /script/load` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SDIFF](actions/sdiff.md) | `GET /sdiff` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SDIFFSTORE](actions/sdiffstore.md) | `GET /sdiffstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SELECT](actions/select.md) | `GET /select` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SET](actions/set.md) | `GET /set` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [Set Key Value](actions/set-key-value.md) | `GET /set/:key/:value` | [docs](https://upstash.com/docs/redis/features/restapi) |
| [SETBIT](actions/setbit.md) | `GET /setbit` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SETEX](actions/setex.md) | `GET /setex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SETNX](actions/setnx.md) | `GET /setnx` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SETRANGE](actions/setrange.md) | `GET /setrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SINTER](actions/sinter.md) | `GET /sinter` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SINTERCARD](actions/sintercard.md) | `GET /sintercard` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SINTERSTORE](actions/sinterstore.md) | `GET /sinterstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SISMEMBER](actions/sismember.md) | `GET /sismember` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SMEMBERS](actions/smembers.md) | `GET /smembers` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SMISMEMBER](actions/smismember.md) | `GET /smismember` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SMOVE](actions/smove.md) | `GET /smove` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SPOP](actions/spop.md) | `GET /spop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SRANDMEMBER](actions/srandmember.md) | `GET /srandmember` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SREM](actions/srem.md) | `GET /srem` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SSCAN](actions/sscan.md) | `GET /sscan` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [STRLEN](actions/strlen.md) | `GET /strlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SUBSCRIBE](actions/subscribe.md) | `GET /subscribe` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SUNION](actions/sunion.md) | `GET /sunion` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [SUNIONSTORE](actions/sunionstore.md) | `GET /sunionstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [TIME](actions/time.md) | `GET /time` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [TOUCH](actions/touch.md) | `GET /touch` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [TTL](actions/ttl.md) | `GET /ttl` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [TYPE](actions/type.md) | `GET /type` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [UNLINK](actions/unlink.md) | `GET /unlink` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [UNSUBSCRIBE](actions/unsubscribe.md) | `GET /unsubscribe` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [UNWATCH](actions/unwatch.md) | `GET /unwatch` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [WATCH](actions/watch.md) | `GET /watch` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XACK](actions/xack.md) | `GET /xack` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XACKDEL](actions/xackdel.md) | `GET /xackdel` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XADD](actions/xadd.md) | `GET /xadd` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XAUTOCLAIM](actions/xautoclaim.md) | `GET /xautoclaim` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XCLAIM](actions/xclaim.md) | `GET /xclaim` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XDEL](actions/xdel.md) | `GET /xdel` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XDELEX](actions/xdelex.md) | `GET /xdelex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XGROUP](actions/xgroup.md) | `GET /xgroup` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XINFO CONSUMERS](actions/xinfo-consumers.md) | `GET /xinfo/consumers` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XINFO GROUPS](actions/xinfo-groups.md) | `GET /xinfo/groups` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XINFO STREAM](actions/xinfo-stream.md) | `GET /xinfo/stream` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XLEN](actions/xlen.md) | `GET /xlen` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XPENDING](actions/xpending.md) | `GET /xpending` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XRANGE](actions/xrange.md) | `GET /xrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XREAD](actions/xread.md) | `GET /xread` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XREADGROUP](actions/xreadgroup.md) | `GET /xreadgroup` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XREVRANGE](actions/xrevrange.md) | `GET /xrevrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [XTRIM](actions/xtrim.md) | `GET /xtrim` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZADD](actions/zadd.md) | `GET /zadd` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZCARD](actions/zcard.md) | `GET /zcard` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZCOUNT](actions/zcount.md) | `GET /zcount` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZDIFF](actions/zdiff.md) | `GET /zdiff` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZDIFFSTORE](actions/zdiffstore.md) | `GET /zdiffstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZINCRBY](actions/zincrby.md) | `GET /zincrby` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZINTER](actions/zinter.md) | `GET /zinter` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZINTERCARD](actions/zintercard.md) | `GET /zintercard` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZINTERSTORE](actions/zinterstore.md) | `GET /zinterstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZLEXCOUNT](actions/zlexcount.md) | `GET /zlexcount` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZMPOP](actions/zmpop.md) | `GET /zmpop` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZMSCORE](actions/zmscore.md) | `GET /zmscore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZPOPMAX](actions/zpopmax.md) | `GET /zpopmax` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZPOPMIN](actions/zpopmin.md) | `GET /zpopmin` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZRANDMEMBER](actions/zrandmember.md) | `GET /zrandmember` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZRANGE](actions/zrange.md) | `GET /zrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZRANGEBYLEX](actions/zrangebylex.md) | `GET /zrangebylex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZRANGEBYSCORE](actions/zrangebyscore.md) | `GET /zrangebyscore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZRANGESTORE](actions/zrangestore.md) | `GET /zrangestore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZRANK](actions/zrank.md) | `GET /zrank` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREM](actions/zrem.md) | `GET /zrem` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREMRANGEBYLEX](actions/zremrangebylex.md) | `GET /zremrangebylex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREMRANGEBYRANK](actions/zremrangebyrank.md) | `GET /zremrangebyrank` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREMRANGEBYSCORE](actions/zremrangebyscore.md) | `GET /zremrangebyscore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREVRANGE](actions/zrevrange.md) | `GET /zrevrange` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREVRANGEBYLEX](actions/zrevrangebylex.md) | `GET /zrevrangebylex` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREVRANGEBYSCORE](actions/zrevrangebyscore.md) | `GET /zrevrangebyscore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZREVRANK](actions/zrevrank.md) | `GET /zrevrank` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZSCAN](actions/zscan.md) | `GET /zscan` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZSCORE](actions/zscore.md) | `GET /zscore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZUNION](actions/zunion.md) | `GET /zunion` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
| [ZUNIONSTORE](actions/zunionstore.md) | `GET /zunionstore` | [docs](https://upstash.com/docs/redis/overall/rediscompatibility) |
