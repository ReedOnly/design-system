# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.14.0] - 2021-09-30

### Added

- New `placement` property for `Snackbar` for more placement variety ([#1488](https://github.com/equinor/design-system/issues/1488))
- "Clear selection" button for `SingleSelect` & `MultiSelect` ([#1411](https://github.com/equinor/design-system/issues/1411))
- `SingleSelect` & `MultiSelect` will show all items when reopnened, with selected items being highlighted ([#1065](https://github.com/equinor/design-system/issues/1065))
- `SingleSelect` & `MultiSelect` will now open on focus ([#1165](https://github.com/equinor/design-system/issues/1165))

### Fixed

- Missing `readOnly` styles for `Textfield` ([#1162](https://github.com/equinor/design-system/issues/1162))
- `Tooltip` should now respect external handlers ([#1558](https://github.com/equinor/design-system/issues/1558))
- `TextField` should now respect external handlers ([#1538](https://github.com/equinor/design-system/issues/1538))
- `Popover` should now only close on `ESC` key when is open ([#1529](https://github.com/equinor/design-system/issues/1529))
- `Breadcrumbs.Breadcrumb` will now be rendered as `span` when `href` is undefined to avoid duplicate `a` elements when used with router libraries ([#1505](https://github.com/equinor/design-system/issues/1505))
- `Snackbar` & `Banner` components should now accept `ref` properties! ([#810](https://github.com/equinor/design-system/issues/810))
- `Tooltip` should now work when used in combination with `Popover` or `Menu` with anchor elements ([#1496](https://github.com/equinor/design-system/issues/1496))
- Adjustments and added missing `compact` styling for `Radio` ([#1580 ](https://github.com/equinor/design-system/pull/1580))

### Changed

- Reduced focus offset for `Button` variant `ghost_icon` ([#1565 ](https://github.com/equinor/design-system/issues/1565))
- Cleaned up styling i `Card.Actions` ([#1520 ](https://github.com/equinor/design-system/issues/1520))
- `Search` & `Accordion` icon sizes are aligned with other components ([#1403](https://github.com/equinor/design-system/issues/1403))
- Adjusted colors for select components ([#1514](https://github.com/equinor/design-system/issues/1514))
- Adjusted focus and label spacing for `Switch` ([#1567](https://github.com/equinor/design-system/issues/1567))

### Removed

- `Snackbar` `leftAlignFrom` property is replaced by `placement` for more placement options. ([#1488](https://github.com/equinor/design-system/issues/1488))

## [0.13.1] - 2021-07-16

### Fixed

- Jest/react-testing-library errors in bundle when using with Webpack 5 ([#1490](https://github.com/equinor/design-system/issues/1490)) & ([#1406](https://github.com/equinor/design-system/issues/1406))
- Snackbar timeout improvements to avoid "missed" timeout ([#1486](https://github.com/equinor/design-system/issues/1486))
- Snackbar centering was wrong when used inside certain elements ([#1172](https://github.com/equinor/design-system/issues/1172))
- Snackbar stacking content order, should now be on top most of the time ([#1173](https://github.com/equinor/design-system/issues/1173))

## [0.13.0] - 2021-07-15

### Added

#### Compact components part 1 ([#1249](https://github.com/equinor/design-system/issues/1249))

- Compact mode can be activated by using the `EdsProvider` as a parent component and setting the `density` property to `"compact"`. This will toggle compact mode on all nested components.
- Components with compact support:
  - `TextField`
  - `Input`
  - `Checkbox`
  - `Menu`
  - `NativeSelect`
  - `SingleSelect`
  - `MultiSelect`
  - `Button`
  - `Switch`
  - `Table`
- Example:

```typescript
// This renders a compact Table with compact Button & Checkbox inside
<EdsProvider density="compact">
  <Table>
    <Table.Body>
      <Table.Row>
        <Table.Cell>
          <Button>Compact</Button>
        </Table.Cell>
      </Table.Row>
      <Table.Row>
        <Table.Cell>
          <Checkbox />
        </Table.Cell>
      </Table.Row>
      ...
    </Table.Body>
  </Table>
</EdsProvider>
```

### Fixed

- `TopBar` missing bottom-border ([#1395](https://github.com/equinor/design-system/issues/1395))
- Wrong types in the `onChange` callback in `Pagination` ([#1397](https://github.com/equinor/design-system/issues/1397))
- Misaligned `Icon` when used inside `Button` variant `ghost_icon` ([#1423](https://github.com/equinor/design-system/issues/1423))
- `TextField` lost focus if `inputIcon` was toggled conditionally ([#1425](https://github.com/equinor/design-system/issues/1425))
- `TextField` with `inputIcon` had wrong border color ([#1425](https://github.com/equinor/design-system/issues/1425))
- Typo in `Accordion` `displayName` ([#1450](https://github.com/equinor/design-system/pull/1450))
- Disabled `Button` was not disabled if `href` was set ([#1456](https://github.com/equinor/design-system/issues/1456))
- Stacking order for overlay components (`Menu`, `Popover`, `Scrim` etc.) ([#1462](https://github.com/equinor/design-system/issues/1462), [#1466](https://github.com/equinor/design-system/issues/1466))

### Changed

- Darker hover background in `Menu` for better accessibility ([#1363](https://github.com/equinor/design-system/issues/1363))
- `Switch` sizes, hover, label spacing and focus frame to match the design in Figma ([#1433](https://github.com/equinor/design-system/issues/1433))
- Optional `label` for `Switch` ([#1445](https://github.com/equinor/design-system/issues/1453)), `Checkbox` ([#1425](https://github.com/equinor/design-system/issues/1453)), `Radio` ([#1459](https://github.com/equinor/design-system/issues/1459))

## [0.12.1] - 2021-05-28

### Fixed 🐛

- Multiline `TextField` did not follow `rowsMax` rules on initial render [(#1367)](https://github.com/equinor/design-system/issues/1367)
- Multiline `TextField` resized on input when having a fixed height [(#1375)](https://github.com/equinor/design-system/issues/1375)
- Wrong spacing in `Button` when an icon was used [(#1364)](https://github.com/equinor/design-system/issues/1364)

### Changed

- Clarified `Radio` story [(#1382)](https://github.com/equinor/design-system/issues/1382)
- Reduced line-height on `Typography` (for `h1`, `h2` & `h3`) [(#1370)](https://github.com/equinor/design-system/issues/1370)

## [0.12.0] - 2021-05-21

### Added

- `TextField` has a new property, `rowsMax` for determining how many rows it will grow before overflow (scrollbars) show [(#1336)](https://github.com/equinor/design-system/issues/1336)

### Fixed 🐛

- `Menu` did not respect anchor position when used with conditional rendering [(#1330)](https://github.com/equinor/design-system/issues/1330)
- Wrong `Tooltip` position if surrounding content would skew its anchor element [(#1331)](https://github.com/equinor/design-system/issues/1331)
- Tweaks to `Menu`, `Popover` & `Tooltip` component and stories in terms of `a11y` use-cases with screen-readers [(#1352)](https://github.com/equinor/design-system/issues/1352)

### Changed

- Improvements to `useCombinedRef` hook [(#1347)](https://github.com/equinor/design-system/issues/1347)
- `Menu` is now using React portals and positioned under `body` [(#1352)](https://github.com/equinor/design-system/issues/1352)
- `Tooltip` is now conditionally rendered internally [(#1341)](https://github.com/equinor/design-system/issues/1341)

## [0.11.1] - 2021-05-06

### Fixed 🐛

- Missing border on "outlined" `Button` ([#1332](https://github.com/equinor/design-system/issues/1332))

## [0.11.0] - 2021-05-05

### Added

- Export types for all sub-components ([#1127](https://github.com/equinor/design-system/issues/1127))

### Fixed 🐛

- Hide `Tooltip` when `title` is empty string ([#1292](https://github.com/equinor/design-system/issues/1292))
- `Tooltip` errors when used in SSR(server-side rendering) ([#1230](https://github.com/equinor/design-system/issues/1230))
- `Tooltip` being stuck when scrolling while open([#1325](https://github.com/equinor/design-system/issues/1325))
- Too big offset on focus-frame for `Button` ([#1218](https://github.com/equinor/design-system/issues/1218))

### Removed

- Sub-components exposed with double names ([#1317](https://github.com/equinor/design-system/issues/1317))

## [0.10.1] - 2021-04-15

### Fixed 🐛

- Missing typescript suggestions on property `placement` ([#1229](https://github.com/equinor/design-system/issues/1229))
- Crashing `Tooltip` component when refreshing using SSR ([#1230](https://github.com/equinor/design-system/issues/1230))

## [0.10.0] - 2021-04-14

### Added ✨

- New `placement` property on `Menu` to define placement of opened `Menu`. List of available values [here](https://eds-storybook-react.azurewebsites.net/?path=/docs/components-menu--default) ([#952](https://github.com/equinor/design-system/issues/952))
- New `anchorEl` property on `Popover`. Use this in combination with `ref` on anchor and `open` on `Popover`. ([#673](https://github.com/equinor/design-system/issues/673))
- New `enterDelay` property on `Tooltip` to delay open ([#1154](https://github.com/equinor/design-system/issues/1154))
- `Tooltip` can now be closed on global `ESC` keypress ([#1195](https://github.com/equinor/design-system/issues/1195))
- `Tooltip` can now be used on `td` elements ([#984](https://github.com/equinor/design-system/issues/984))

### Changed 📓

- `Menu`, `Popover` and `Tooltip`
  - Improved popup logic with the use of [popperJS](https://popper.js.org/) ([#673](https://github.com/equinor/design-system/issues/673))
- Streamlined close logic for
  - `Menu`, `Popover` and `Scrim` ([#1175](https://github.com/equinor/design-system/issues/1175))
- `Menu` property `anchorEl` changed from required to optional ([#1193](https://github.com/equinor/design-system/issues/1193))

### Fixed 🐛

- Missing focus frame on `Breadcrumbs` ([#1134](https://github.com/equinor/design-system/issues/1134))
- Missing props table for `Menu` in Storybook ([#1164](https://github.com/equinor/design-system/issues/1164))
- Missing role on `Banner`([#1178](https://github.com/equinor/design-system/issues/1178))
- Clarified use of `Banner.Actions` in Storybook ([#1188](https://github.com/equinor/design-system/issues/1188))
- Missing focus frame on `Typography` links ([#1203](https://github.com/equinor/design-system/issues/1203))
- Missing disabled colours on `TextField` ([#1161](https://github.com/equinor/design-system/pull/1161))
- Wrong offset on `Button` focus frame ([#1218](https://github.com/equinor/design-system/pull/1218))

### Breaking changes ⚠️

- `Placement` values in `Tooltip` and `Popover` are changed to match [popperJS](https://popper.js.org/). List of available values [here](https://eds-storybook-react.azurewebsites.net/?path=/docs/components-popover--default)
- `Popover.Anchor` deprecated, please use the `anchorEl` property on `Popover` instead.
- Removed `open` property on `Tooltip` as it was not working as expected

### Deprecated 🗑

- `Popover.Anchor` deprecated due to streamlined popup logic

## [0.9.2] - 2021-03-19

### Fixed

- Bumped eds-tokens version

## [0.9.0] - 2021-03-17

### Added ✨

- TextField ([#1107](https://github.com/equinor/design-system/issues/1107), [#1108](https://github.com/equinor/design-system/issues/1108), [#1111](https://github.com/equinor/design-system/issues/1111), [#1115](https://github.com/equinor/design-system/issues/115), [#1131](https://github.com/equinor/design-system/issues/1131), [#1128](https://github.com/equinor/design-system/issues/1128))
  - `Input` and `Label` is now available as separate components. This will make it easier to customize for more advanced patterns or for making your own custom components for specialized use-cases.
  - `TextField` now support `unit` inside the input field. This is useful for e.g. currency and units of measurement.

### Changed 📓

- Textfield
  - Improvements when using the `Icon` in the `inputIcon` and `helperIcon` props. This makes the behaviour here more similar to the rest of the EDS library. ([#1130](https://github.com/equinor/design-system/issues/1130))
  - Internal fixes and optimization

### Fixed 🐛

- Textfield
  - Fixed missing disabled colors ([#1160](https://github.com/equinor/design-system/issues/1160))

## [0.8.5] - 2021-02-22

### Added ✨

- Progress indicators ([#1090](https://github.com/equinor/design-system/issues/1090), [#1098](https://github.com/equinor/design-system/issues/1098))
  - `Circular`, `Star` and `Dots` now have a `size` property for adjusting size.
  - `Circular` and `Dots` now have a `color` property following the same color scheme as our other components.
  - Refactored as compound components. You can now find the progress indicators under `Progress`, such as `Progress.Dots`, `Progress.Star` etc..
    - The individual `LinearProgress`, `CircularProgress`, `StarProgress` & `DotProgress` will be removed at a later time
- `Accordion.Header` now has an `onToggle` callback to help defer rendering of content when `Accordion` are opened/closed ([#1121](https://github.com/equinor/design-system/pull/1121))

### Fixed 🐛

- Adjusted text and icon placements inside `Button` so that `Icon` (svg) will always align to the sides regardless of button width ([#1085](https://github.com/equinor/design-system/issues/1085))
- Fixed `Menu` story where content would skew the `MenuItem` height (#1104)
- Progress indicators ([#1090](https://github.com/equinor/design-system/issues/1090), [#1098](https://github.com/equinor/design-system/issues/1098))
  - Adjustments so that `Circular` and `Dots` can be used inside `Button`
  - Cleaned up component so that they are pure svgs now (except for `Linear`)

### Changed 📓

- Cleaned up sub-component naming, so no more repeating names such as, `Card.CardActions` or `Menu.MenuSection` ([#1083](https://github.com/equinor/design-system/issues/1083))
  - The old sub-component names are still there but will be removed at a later time
- Updated our storybook stories to better reflect usages of components with sub-components ([#1094](https://github.com/equinor/design-system/issues/1094))

### Deprecated

- Progress indicators ([#1090](https://github.com/equinor/design-system/issues/1090))
  - Removed `variant` property on `Dots` (replaced by `color` property)
- `Button` do no longer force size on nested `Icon`

## [0.8.4] - 2021-01-21

### Added ✨

- Active, error and hover states in `Table` ([#940](https://github.com/equinor/design-system/issues/940))
- Support for toggling sortable Table column styling. New property `sort` on `Table.Cell` ([#983](https://github.com/equinor/design-system/issues/983))
- Sticky Table head (#1031). New property `sticky` on `Table.Head`

### Fixed 🐛

- Tests for Table ([#297](https://github.com/equinor/design-system/issues/297))
- Missing primary color on `Button` `variant="ghost_icon"` ([#986](https://github.com/equinor/design-system/issues/986))
- Hover bug on touch devices ([#987](https://github.com/equinor/design-system/issues/987))
- Icon bug in Storybook when changing name ([#955](https://github.com/equinor/design-system/issues/955))
- `SingleSelect` items are properly updated when changed after initial render (#1064)

### Changed 📓

- Improved `Table.Cell` ([#997](https://github.com/equinor/design-system/issues/997))
- Refactored Table to use React.forwardRef (#1007)

### Deprecated

- `Table.Cell` `as` property on is removed. This had to be done due to technical limitations with new features. `Table.Cell` will now automatically render `th` or `td` based on "parent" element.

## [0.8.3] - 2020-12-14

### Fixed

- Fixed unintended full width on `<Button />` ([#](https://github.com/equinor/design-system/pull/976))

## [0.8.2] - 2020-12-11

### Fixed

- Use newest versions of @equinor/eds-icons and @equinor/eds-tokens

## [0.8.0] - 2020-12-09

### Added ✨

- `SingeSelect` component ([#896](https://github.com/equinor/design-system/issues/896))
- `MultiSelect` component ([#897](https://github.com/equinor/design-system/issues/897))

### Fixed 🐛

- Fix wrong spacings inside `Chip` causing the content to not be proper centered ([#956](https://github.com/equinor/design-system/issues/956))
- Hover size on ghost buttons ([#595](https://github.com/equinor/design-system/issues/595))

### Changed 📓

- Use base tokens in `Button` component ([#831](https://github.com/equinor/design-system/issues/831))
- Use base tokens in `Table` component ([#830](https://github.com/equinor/design-system/issues/830))
- Support for React 17 ([#813](https://github.com/equinor/design-system/issues/813))
- Update dependencies ([#904](https://github.com/equinor/design-system/issues/904))

## [0.7.1] - 2020-11-26

### Changed 📓

- Updated README.md

## [0.7.0] - 2020-11-26

### Added ✨

- Types, as part of the [Typescript Milestone](https://github.com/equinor/design-system/milestone/7?closed=1)
- `NativeSelect` component ([#509](https://github.com/equinor/design-system/issues/509))
- `Table` caption ([#621](https://github.com/equinor/design-system/issues/621))
- `isExpanded` prop to control `Accordion` externally ([#677](https://github.com/equinor/design-system/issues/677))

### Fixed 🐛

- Added a guard clause to handle null values for `Accordion` children ([#688](https://github.com/equinor/design-system/issues/688))
- `CardMedia` spacing bug ([#603](https://github.com/equinor/design-system/issues/603))
- Added props spread to `BannerAction` ([#478](https://github.com/equinor/design-system/issues/478))
- `Pagination` bug ([#647](https://github.com/equinor/design-system/issues/647))
- Bundle improvements ([#627](https://github.com/equinor/design-system/issues/627))
- Cleaned up leaking `devDependencies` ([#862](https://github.com/equinor/design-system/issues/862))
- Hide `Tooltip` when title is empty ([#920](https://github.com/equinor/design-system/issues/920))

### Changed 📓

- Updated `z-index` values for correct layering of the components ([#872](https://github.com/equinor/design-system/issues/872))
- Changed licence from GNU AGPL to MIT ([#852](https://github.com/equinor/design-system/issues/852))
- Clean up use of spacings in `Card` ([#717](https://github.com/equinor/design-system/issues/717))
- Changed module types for better support with `commonjs` and `esm`. Using the `<some-eds-npm-package>/commonjs` path on packages should no longer be needed and will be deprecated in the future ([#887](https://github.com/equinor/design-system/issues/887))
- Removed unused dependencies ([#870](https://github.com/equinor/design-system/issues/870))
- Cleaning and remodelling core-react for the future 💅 ([#887](https://github.com/equinor/design-system/issues/887))

## [0.6.2] - 2020-09-16

### Fixed 🐛

- Fixed `onClose` handler not being called when `MenuItem` was used inside `MenuSection` ([#546](https://github.com/equinor/design-system/issues/546))
- Fixed focus showing when clicking on `MenuItem` ([#544](https://github.com/equinor/design-system/issues/544))
- Fixed an issue where `Divider` did not stretch to full width ([#608](https://github.com/equinor/design-system/issues/608))
- Fixed `Head` styling when `Table` is set to `width: 100%` ([#610](https://github.com/equinor/design-system/issues/610))

### Changed

- Added outside click support for closing `Menu`. Outside clicks will now call the `onClose` handler function. ([#548](https://github.com/equinor/design-system/issues/548))
- Added `data` property to `Icon` component to easily compose icon to be rendered. ([#584](https://github.com/equinor/design-system/issues/584))
  - See `Icon` [README](https://github.com/equinor/design-system/tree/develop/libraries/core-react/src/Icon) for more information

## [0.6.1] - 2020-09-04

### Fixed 🐛

- Loosened up on Tabs & TabsPanel typechecking for children ([#539](https://github.com/equinor/design-system/issues/539))

## [0.6.0] - 2020-09-02

### Added

- `<Menu>` component
- `<Pagination>` component

### Fixed 🐛

- Changed background color on `<Tabs>` to transparent ([#533](https://github.com/equinor/design-system/pull/533))
- Improved tooltip inconsistencies when used inside a table ([#488](https://github.com/equinor/design-system/pull/488))
- Fixed Tooltip triggering on some disabled elements ([#479](https://github.com/equinor/design-system/pull/479))
- Fixed misplaced text when using `<Button>` as link or upload ([#482](https://github.com/equinor/design-system/issues/482))
- Fixed wrong color on action buttons in snackbar ([#535](https://github.com/equinor/design-system/issues/535))
- Fixed elevation for dialog ([#534](https://github.com/equinor/design-system/issues/517))

## [0.5.1] - 2020-07-15

### Changed

- Font-weight has been increased to medium in all cases where the font-size is below 16px for improved legibility. This change is most notable in table cells and labels.
- Font-size has been increased and line-height decreased for `<helper>` and `<label>`
- `<Icon>` now uses `currentColor` for its fill value – which means it inherits its fill colour from its parents `color` value
- `<Typography>` now accepts any value for its color property

## [0.4.1] - 2020-07-13

### Added

- `<Typography>` can now limit the number of visible lines, render any typography style in EDS, change the underlying html element and override/extend tokens used for a particular variant
- `<Table>` can now have headers in columns in the table body

### Fixed 🐛

- Fixed horizontal alignment of icons and unintended border-color in `<Button>` in Safari ([#465](https://github.com/equinor/design-system/issues/465))
- Fixed the “off”-colour in `<Switch>`([#466](https://github.com/equinor/design-system/issues/466))
- Fixed an alignment bug in `<Tooltip>`([#408](https://github.com/equinor/design-system/issues/408))
- Fixed alignment of headers in `<Table>`([#407](https://github.com/equinor/design-system/issues/407))

## [0.4.0] - 2020-06-25

### Added

- Breadcrumbs
- Progress
- Snackbar
- `<Button>` can now be rendered as an `<a>` by providing an `href` attribute
- Support for left/right icons inside `<Button`

### Fixed

- Fixed an overflow bug in `<Popover>`([#375](https://github.com/equinor/design-system/issues/375))

### Changed

- Increased `<Button>` icon size to 24px (up from 16px) for greater legibility
- README
  - Moved Progress indicator, Breadcrumbs, Snackbar and Button variations with icons to «Available»
  - Moved Pagination to «In progress»

## [0.3.1] - 2020-06-16

### Fixed

- Fixed a bug where `<Tabs>` steals focus from interactive controls in tab panels. ([#369](https://github.com/equinor/design-system/issues/369))

## [0.3.0] - 2020-06-08

### Added

- Banner
- Popover
- Slider
- Selection controls
- Option to control the `<Search>` component. ([#342](https://github.com/equinor/design-system/issues/342))

### Fixed 🐛

- Fixed a bug where `<Tooltip>` did not close as expected. ([#339](https://github.com/equinor/design-system/issues/339))

### Changed

- README
  - Moved Banner, Popover, Selection controls and Slider to «Available»
  - Moved Progress indicator and Snackbar to «In progress»

## [0.2.2] - 2020-06-02

### Fixed 🐛

- Fixed bug where `<Tabs>` component focused automatically on the active tab on render. ([#329](https://github.com/equinor/design-system/issues/329))

## [0.2.1] - 2020-05-29

### Fixed 🐛

- Fixed bug where `<Search>` component ignored `onFocus` & `onBlur` functions. ([#330](https://github.com/equinor/design-system/issues/330))

## [0.2.0] - 2020-04-30

### Added

- Card
- Tooltip

### Fixed

- `<Button>` component property `type` can now correctly be overridden

### Changed

- README
  - Moved Card and Tooltip to «available»
  - Moved Slider and Popover to «in progress»

## [0.1.4] - 2020-04-20

### Fixed

- Republished with pnpm to fix "workspace:\*" pointers in package.json

## [0.1.3] - 2020-04-16

### Added

- Accordion
- Search
- Table of contents
- Dialog
- Scrim
- Polyfill for :focus-visible

### Changed

- README
  - Moved Accordion, Search, Table of contents, Dialog and Scrim to «available»
  - Moved Tooltip, Navigation Drawer, Menu to «in progress»

## [0.1.2] - 2020-03-23

### Added

- Chips
- Sidesheet

### Changed

- README
  - Moved Chips and Side sheet to «available»
  - Moved Cards, Table of contents, Search and Scrim to «in progress»

## [0.1.1] - 2020-03-11

### Added

- Tabs

### Changed

- README
  - Sorted components alphabetically
  - Moved Tabs to «available»
  - Moved Chips, Dialog and Side Sheet to «in progress»

## [0.1.0] - 2020-02-24

### Added

New components

- Button
  - Ghost icon variant
- List
- TopBar
- Icon
- Tabs

### Changed

- Updated README to me abit more clearer
- Adjustments to to `package.json` to be more in line with our other packages
- New versioning of packages

## [0.0.1-alpha.10] - 2020-01-22

### Fixed

- Faulty build configuration forcing use of umd modules for
- Missing package settings and deprecated npm-script commands
- Malformed changelog

## [0.0.1-alpha.9] - 2020-01-13

### Added

- Textfield alpha component

## [0.0.1-alpha.8] - 2020-01-10

### Changed

- Updated build (wups)

## [0.0.1-alpha.7] - 2020-01-10

### Added

New alpha components:

- Divider
- Table
- Typography

## [0.0.1-alpha.6] - 2019-08-12

### Fixed

- Typo in changelogs

## [0.0.1-alpha.5] - 2019-08-12

### Added

- `@equinor/eds-tokens` as a dependency for tokens

## [0.0.1-alpha.4] - 2019-07-09

### Changed

- Update README

## [0.0.1-alpha.3] - 2019-07-08

### Changed

- Update README

## [0.0.1-alpha.2] - 2019-07-08

### Changed

- Update README
- Add CHANGELOG

## [0.0.1-alpha.1] - 2019-07-08

### Changed

- Publish alpha-version of library
- Copy tokens temporarily to src/tokens
