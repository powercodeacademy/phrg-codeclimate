# Codeclimate

[Codeclimate](https://codeclimate.com/) is tool Power uses to analyze code health. Similar to `overcommit`, `codeclimate` is run as a hook. However, instead of on a hook on local git commits like `overcommit`, `codeclimate` is executed as a [Github webhook](https://help.github.com/articles/about-webhooks/). This means that codeclimate results show up on Github PRs themselves. For Nitro, it is required that codeclimate analysis is successful to merge a pull request into `nitro-web`'s master branch.

#### Successful Codeclimate Github Report

![Passing Codeclimate Check](https://raw.githubusercontent.com/powerhome/phrg-codeclimate/master/successful-codeclimate-check.png?raw=true "Passing Codeclimate Check")

#### Failing Codeclimate Github Report

![Failing Codeclimate Check](https://raw.githubusercontent.com/powerhome/phrg-codeclimate/master/failing-codeclimate-check.png?raw=true "Failing Codeclimate Check")

## Codeclimate Analysis

Like many tools we have learned about already, `codeclimate` is configurable. So what codeclimate analyzes depends upon what is enabled by our team.

Codeclimate configuration lives in a `.codeclimate.yml` file that lives in the root directory of `nitro-web`. At the time of writing, Nitro's codeclimate runs linting on CSS files using `csslint`, Javascript files using `eslint`, and Coffeescript files using `coffeelint`. Codeclimate could also be configured to run Ruby linting with `rubocop`, but `overcommit` already takes care of this.

To get the full picture of what codeclimate does and does not analyze, visit the [Codeclimate documentation](https://docs.codeclimate.com/) and review Nitro's `.codeclimate.yml`.

## Codeclimate Interface

## Resources

- [Codeclimate](https://codeclimate.com/)
- [Codeclimate Documentation](https://docs.codeclimate.com/)
- [Github webhooks](https://help.github.com/articles/about-webhooks/)
- [Thoughtbot article on Codeclimate](https://thoughtbot.com/work/code_climate)
