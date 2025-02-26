# renovate-config

> Alma's Renovate Sharable Configuration

For more see [Renovate Docs][renovate-config-presets].

> [!NOTE] Renovate has been deprecating npm-based presets in favor of
> repository hosting presets. This repository is migrated
> [`@lmc-eu/renovate-config` package][renovate-npm-package] which is now
> deprecated. [Original source][renovate-package-source] is available at [Code
> Quality Tools repository][code-quality-tools].

## 🚀 Usage

Enable Renovate in your repository and just `extends` in `.renovaterc.json`.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>alma-oss/renovate-config"]
}
```

[You can use][renovate-local-presets] `local` instead of `github` if you are on
the same platform.

## 🎛️ Presets

### Default

Default preset

```json
{
  "extends": ["github>alma-oss/renovate-config"]
}
```

### Schedule

#### Weekly

Starting on Monday so you will have the weekend to resolve the dependency
updates.

##### Non-office Hours

```json
{
  "extends": ["github>alma-oss/renovate-config:scheduleWeeklyNonOfficeHours"]
}
```

##### Business Hours

```json
{
  "extends": ["github>alma-oss/renovate-config:scheduleWeeklyBusinessHours"]
}
```

#### Every Two Weeks

Starting on Monday on the 2nd and 4th instance so you will have 2 weeks to
resolve the dependency updates.

This is most useful for two weeks sprints.

##### Non-office Hours

```json
{
  "extends": [
    "github>alma-oss/renovate-config:scheduleEveryTwoWeeksNonOfficeHours"
  ]
}
```

##### Business Hours

```json
{
  "extends": [
    "github>alma-oss/renovate-config:scheduleEveryTwoWeeksBusinessHours"
  ]
}
```

### Group

#### Major Production Dependencies

```json
{
  "extends": ["github>alma-oss/renovate-config:groupMajorProdDependencies"]
}
```

#### Non-Major Production Dependencies

```json
{
  "extends": ["github>alma-oss/renovate-config:groupNonMajorProdDependencies"]
}
```

#### All Development Dependencies

```json
{
  "extends": ["github>alma-oss/renovate-config:groupAllDevDependencies"]
}
```

## 🙌 Contributing

We're always looking for contributors to help us fix bugs, build new features,
or help us improve the project documentation. If you're interested, definitely
check out our [Contributing Guide][contributing]! 👀

## 📝 License

See the [LICENSE][license] file for information.

[code-quality-tools]: https://github.com/lmc-eu/code-quality-tools/
[contributing]: ./CONTRIBUTING.md
[license]: ./LICENSE.md
[renovate-config-presets]: https://docs.renovatebot.com/config-presets/
[renovate-local-presets]: https://docs.renovatebot.com/config-presets/#local-presets
[renovate-npm-package]: https://www.npmjs.com/package/@lmc-eu/renovate-config
[renovate-package-source]: https://github.com/lmc-eu/code-quality-tools/tree/main/packages/renovate-config
