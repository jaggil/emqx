# 5.0.1

## Enhancements

* Removed management API auth for prometheus scraping endpoint /api/v5/prometheus/stats [8299](https://github.com/emqx/emqx/pull/8299)
* Added more TCP options for exhook (gRPC) connections. [8317](https://github.com/emqx/emqx/pull/8317)
* Allow http authz backend to return a HTTP body to indicate result `deny` | `allow` or `ignore`. [8377](https://github.com/emqx/emqx/pull/8377)
* Bulk subscribe/unsubscribe APIs [8356](https://github.com/emqx/emqx/pull/8356)
* Added exclusive subscription [8315](https://github.com/emqx/emqx/pull/8315)
* Improve authn failure/error counter metrics [8352](https://github.com/emqx/emqx/pull/8377) [8375](https://github.com/emqx/emqx/pull/8352)
* Do not allow admin user self-deletion [8286](https://github.com/emqx/emqx/pull/8286)
* After restart, ensure to copy `cluster-override.conf` from the clustered node which has the greatest `tnxid`. [8333](https://github.com/emqx/emqx/pull/8333)

## Bug fixes

* A bug fix ported from 4.x: allow deleting subscriptions from `client.subscribe` hookpoint callback result. [8304](https://github.com/emqx/emqx/pull/8304) [8347](https://github.com/emqx/emqx/pull/8377)
* Fixed Erlang distribution over TLS [8309](https://github.com/emqx/emqx/pull/8309)
* Made possible to override authentication configs from environment variables [8323](https://github.com/emqx/emqx/pull/8309)
* Made authentication passwords in Mnesia database backward compatible to 4.x, so we can support data migration better. [8351](https://github.com/emqx/emqx/pull/8351)

* Fix plugins upload for rpm/deb installations [8379](https://github.com/emqx/emqx/pull/8379)
* Sync data/authz/acl.conf and data/certs from clustered nodes after a new node joins the cluster [8369](https://github.com/emqx/emqx/pull/8369)
* Ensure auto-retry of failed resources [8371](https://github.com/emqx/emqx/pull/8371)
* Fix matrics name `connack.auth_error` -> `packets.connack.auth_error` [8178](https://github.com/emqx/emqx/pull/8178)

## Others

* Rate limiter interface is hidden so far, it's subject to a UX redesign.
* QUIC library upgraded to 0.0.14.
* Now the default packages will be released withot otp version number in the package name.
* Renamed config exmpale file name in `etc` dir.