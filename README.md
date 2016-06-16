[![NPM version](https://badge.fury.io/js/tslint-react.svg)](https://www.npmjs.com/package/tslint-react)
[![Downloads](http://img.shields.io/npm/dm/tslint-react.svg)](https://npmjs.org/package/tslint-react)
[![Circle CI](https://circleci.com/gh/palantir/tslint-react.svg?style=svg)](https://circleci.com/gh/palantir/tslint-react)

tslint-react
------------

Lint rules related to React & JSX for [TSLint](https://github.com/palantir/tslint/).

### Rules

- `jsx-no-lambda`
  - Creating new anonymous functions (with either the `function` syntax or ES2015 arrow syntax) inside the `render` call stack works against _pure component rendering_. When doing an equality check between two lambdas, React will always consider them unequal values and force the component to re-render more often than necessary.
  - Rule options: _none_
- `no-string-ref`
  - Passing strings to the `ref` prop of React elements is considered a legacy feature and will soon be deprecated.
    Instead, [use a callback](https://facebook.github.io/react/docs/more-about-refs.html#the-ref-callback-attribute).
  - Rule options: _none_

### Development

We track rule suggestions on Github issues -- [here's a useful link](https://github.com/palantir/tslint-react/issues?q=is%3Aissue+is%3Aopen+label%3A%22Type%3A+Rule+Suggestion%22) to view all the current suggestions. Tickets are roughly triaged by priority (P1, P2, P3).

We're happy to accept PRs for new rules, especially those marked as [Status: Accepting PRs](https://github.com/palantir/tslint-react/issues?q=is%3Aissue+is%3Aopen+label%3A%22Status%3A+Accepting+PRs%22). If submitting a PR, try to follow the same style conventions as the [core TSLint project](https://github.com/palantir/tslint).