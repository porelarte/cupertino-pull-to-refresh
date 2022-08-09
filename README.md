<p align="center">
<img src="" height="100" alt="Bloc" />
</p>
<h2 align="center">cupertino_refresh</h2>


## Motivation behind the package

While developing one of my client's mobile application I felt a need for a UI component for the purpose that whenever the user wants to refresh the page, he/she should be able to trigger an all-over start for the screen and its data instead of going back and reopening the screen. By using `RefreshIndicator` which is included in the `material` package of Flutter the mission was achieved. But, it was, seemingly, exotic on iOS devices. I felt a need, the need for an iOS-like refresh indicator, which turned out to be included in the `cupertino` package of Flutter as `CupertinoRefreshSliver`. 

So, why package then? 🤔

You see, `CupertinoRefreshSliver` is a sliver which means in order to be able to use it you have to use `CustomScrollView` to layout your widgets and `Sliver`s for everything, although, if not for everything but at least with wrapping widgets inside of a `SliverToBoxAdapter`, yet, always, `Sliver`s are there. But who wants to refactor every screen, page, or whatever metric you have for view just to have iOS-like refresh control? I didn't, so I've created a workaround which I call: the `CupertinoRefresh` widget.

PS: If you're already using `CustomScrollVeiew` for the layout you can use `CupertinoRefreshSliver` directly as the first element of your `Sliver`s list. See example below.

## Dart Versions

- Dart 2: >= 2.12

## Examples

- [Counter](https://github.com/felangel/bloc/tree/master/packages/bloc/example) - an example of how to create a `CounterBloc` in a pure Dart app.

## Maintainers

- [Felix Angelov](https://github.com/felangel)