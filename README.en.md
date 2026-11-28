# eCharts for Symcon

Use **eCharts** to display live readings, archived measurements and relationships
between Symcon objects. The library includes 32 chart modules and one shared
gateway. Each chart can appear as a Symcon tile or in an IPSView WebContent
widget. Apache ECharts and its themes are bundled with the library.

[Deutsche Anleitung und Modulübersicht](README.md)

## Install and create your first chart

1. In Symcon 9.0 or later with PHP 8.5, open the **Module Store**, search for
   **eCharts** and install the library. If you already use the beta, use the
   existing Store entry for updates and keep your configured charts.
2. To plot today's temperature, create an **EChartsTimeSeries** instance.
   Select your existing **EChartsGateway** as its parent or create one with
   your first chart. Further charts can share the same gateway.
3. Add your temperature variable as a source, select a period covering today
   and click **Apply**. Historical charts need readings already recorded by
   Archive Control. For a current reading, **EChartsGaugeSingle** needs only
   a numeric variable.
4. Open the chart instance in the tile visualization. To use it in IPSView,
   enable the IPSView HTML output, click **Apply** and add the generated string
   variable to IPSView as WebContent. IPSView is optional.

## Choose and style a chart

Use **EChartsTimeSeries** for lines or stacked areas, **EChartsBarHistory** for
historical bars and **EChartsStateTimeline** for changes such as open and closed
windows. For wind direction, **EChartsGaugeWind** offers 37 compass rose presets
and accepts a custom SVG. A fixed pointer can show the direction as the rose turns.
The [full module list](README.md#enthaltene-module) links to each module's German guide.

The tile and IPSView designers use the same sources. IPSView initially inherits
the tile design. To edit it separately, copy the tile design into the IPSView
designer. The preview includes unsaved tile settings. Click **Apply** to save.

## Import an existing JSLive chart

1. In JSLive 0.113 or a later compatible release, use the **eCharts migration
   export** to save the chart package (contract 1.0).
2. Open **EChartsGateway**, load the package into the import preview and check
   the proposed target and source assignments. For exports from another
   installation, select the matching local variables and archives.
3. Choose the target category, review the reported differences and confirm
   creation of the new chart. Open its tile alongside your JSLive original.
   The import reuses the assigned sources and their available history. It leaves
   the original chart, variable values and archive records in place.

The [migration walkthrough and comparison gallery](docs/JSLIVE_MIGRATION.md)
show the forms and example results. See the [changelog](CHANGELOG.md) for release
history and the [community topic](https://community.symcon.de/t/144844) for feedback.

## License

The project's own contributions use the [PolyForm Noncommercial License 1.0.0](LICENSE).
Bundled third-party components are covered by their [respective licenses](THIRD_PARTY_NOTICES.md).
