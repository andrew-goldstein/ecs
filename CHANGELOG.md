# CHANGELOG
All notable changes to this project will be documented in this file based on the [Keep a Changelog](http://keepachangelog.com/) Standard. This project adheres to [Semantic Versioning](http://semver.org/).

## Unreleased

### Breaking changes
* Changed `device.*` fields to `observer.*` fields to eliminate user confusion. #238

* Rename `network.total.bytes` to `network.bytes` and `network.total.packets`
  to `network.packets`. #179
* Remove `network.inbound.bytes`, `network.inbound.packets`,
  `network.outbound.bytes` and `network.outbound.packets`. #179
* Changed the `event.type` definition to be only reserved. #242

### Bugfixes

* Fix obvious mistake in the definition of "source", where it said "destination"
  instead of "source". #211

### Added
* Add `host.name` field and clarify usage of `host.hostname`. #187
* Add `event.start` and `event.end` date fields. #185
* Add `process.thread.id` field. #200
* Add `host.name` field and clarify usage of `host.hostname`.
* Add `event.start` and `event.end` date fields.
* Create new `related` field set with `related.ip`. #206
* Add `user.group` field. #204
* Create new `group` field set with `group.id` and `group.name`. #203
* Add `url.full` field. #207
* Add `process.executable` field. #209
* Add `process.working_directory` and `process.start`. #215
* Reintroduce `http`. #237
* Add `user.full_name` field. #201
* Add `network.community_id` field. #208
* Add fields `geo.country_name` and `geo.region_iso_code`. #214
* Add `event.kind` and `event.outcome`. #242
* Add `client` and `server` objects and fields. #236
* Reintroduce a streamlined `user_agent` field set. #240
* Add `geo.name` for ad hoc location names. #248
* Add `event.timezone` to allow for proper interpretation of incomplete timestamps. #258

### Improvements
* Improved the definition of the file fields #196
* Improved the definition of the agent fields #192
* Improve definition of events, logs, and metrics in event section #194
* Improved the definition of network fields in intro section #197
* Improved the definition of host fields #195
* Improved the definitions for `event.category` and `event.action`. #242
* Clarify the semantics of `network.direction`. #212
* Add `source.bytes`, `source.packets`, `destination.bytes` and `destination.packets`. #179

### Deprecated

## [1.0.0-beta1](https://github.com/elastic/ecs/compare/v0.1.0...v1.0.0-beta1)

### Breaking changes
* Change structure of URL. #7
* Rename `url.href` `multi_field`. #18
* Rename `geoip.*` to `geo`. #58
* Rename log.message to log.original. #106
* Rename `event.raw` to `event.original`. #107
* Rename `user_agent.raw` to `user_agent.original` and make it a keyword. #107
* Rename `file.path.raw` to `file.path.keyword`, `file.target_path.raw` to `file.target_path.keyword`,
  `url.href.raw` to `url.href.keyword`, `url.path.raw` to `url.path.keyword`,
  `url.query.raw` to `url.query.keyword`, and `network.name.raw` to `network.name.keyword`. #103
* Remove `log.offset` and `log.line` as too specific for ECS. #131
* Remove top level objects `kubernetes` and `tls`. #132
* Remove `*.timezone.offset.sec` fields as too specific for ECS at the moment. #134
* Make the following fields keyword: device.vendor, file.path, file.target_path, http.response.body, network.name, organization.name, url.href, url.path, url.query, user_agent.original
* Rename `url.host.name` to `url.hostname` to better align with industry convention. #147
* Make the following fields keyword: device.vendor, file.path, file.target_path, http.response.body, network.name, organization.name, url.href, url.path, url.query, user_agent.original. #137
  * Only two fields using `text` indexing at this time are `message` and `error.message`.
* Rename `host.name` to `host.hostname` to better align with industry convention. #144
* Update definition of `service.type` and `service.name`.
* Redefine purpose of `agent.name` field to be user defined field.
* Rename `url.href` to `url.original`.
* Remove `source.subdomain` and `destination.subdomain` fields.
* Rename `event.version` to `ecs.version`. #169
* Remove the `http` field set temporarily. #171
* Remove the `user_agent` field set temporarily. #172
* Rename `url.hostname` to `url.domain`. #175
* Remove `source.hostname` and `destination.hostname`. #175

### Added
* Add `network.total.packets` and `network.total.bytes` field. PR#2
* Add `event.action` field. #21
* Add `network.name`, to track network names in the monitoring pipeline. #25
* Adds cloud.account.id for top level organizational level. #11
* Add `http.response.status_code` and `http.response.body` fields. #4
* Add fields for Operating System data. #5
* Add `log.message`. #3
* Add http.request.method and http.version
* Add `host.os.kernel` containing the OS kernel version. #60
* Add `agent.type` field.
* Add `http.request.referrer` field. #164
* Add `network.type`, `network.iana_number`, `network.transport` and
  `network.application`. #81 and #170

### Improvements

* Remove duplicate definitions of the reuseable `os` field set from `host.os` and
  `user_agent.os`.  #168

## 0.1.0

Initial draft release
