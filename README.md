# Telemetría    [![Kantox ❤ OSS](https://img.shields.io/badge/❤-kantox_oss-informational.svg)](https://kantox.com/)  ![Test](https://github.com/am-kantox/telemetria/workflows/Test/badge.svg)  ![Dialyzer](https://github.com/am-kantox/telemetria/workflows/Dialyzer/badge.svg)

**The helper application that simplifies and standardizes telemetry usage.**

## Installation

```elixir
def project do
  [
    compilers: [:telemetria | Mix.compilers()]
  ]
end

def deps do
  [
    {:telemetria, "~> 0.1"}
  ]
end
```

## Changelog

- **`0.9.1`** —
  - [ENH] `@telemetria process_info: true` keyword parameter
  - [ENH] `@id` is set to the correct `otp_app`
  - [ENH] `MFA` is set properly for alerts
  - [ENH] arguments and result are grouped under `:call`
  - [ENH] total metadata cleanup
- **`0.9.0`** —
  - [ENH] add `Telemetria.Formatter` that can be used to produce JSON logs basing on metadata, natively integrated into `telemetría`
- **`0.8.0`** —
  - [ENH] add `applications` option accepting a keyword list of applications to enable `telemetria` for (with optional parameters)
- **`0.7.0`** —
  - [ENH] add named arguments in all calls to event’s context
- **`0.6.1`** —
  - [BUG] wrong order using telemetry with many clauses
- **`0.6.0`** —
  - [ENH] accept parameters in annotation `@telemetria`
  - [MIN] better print of events added
- **`0.5.2`** —
  - [ENH] `enabled: false` config to purge all telemetria code at once
- **`0.5.1`** —
  - [ENH] add result of underlying call to metric
  - [ENH] decrease an amount of garbage returned from caller context
- **`0.5.0`** —
  - [ENH] annotation `@telemetria true` as a synonym to `deft/2`
  - [FIX] polling is off by default
- **`0.4.0`** —
  - [ENH] default polling of system / vm states for free
  - [ENH] starting in phases ensuring proper instrumenter setup
- **`0.3.0`** —
  - [ENH] no need for any config in any environment
  - [BUG] proper handling of guards in compiler, correct event names

## [Documentation](https://hexdocs.pm/telemetria).
