# Codeclimate

[Codeclimate](https://codeclimate.com/) is a tool Power uses to analyze code health. Similar to `overcommit`, `codeclimate` is run as a hook. However, instead of on a hook on local git commits (like `overcommit`), `codeclimate` is executed as a [Github webhook](https://help.github.com/articles/about-webhooks/). This means that Codeclimate results show up on Github PRs themselves. For Nitro, it's required that Codeclimate analysis is successful to merge a pull request into `nitro-web`'s master branch.

#### Successful Codeclimate Github Report

![Passing Codeclimate Check](https://raw.githubusercontent.com/powerhome/phrg-codeclimate/master/successful-codeclimate-check.png?raw=true "Passing Codeclimate Check")

#### Failing Codeclimate Github Report

![Failing Codeclimate Check](https://raw.githubusercontent.com/powerhome/phrg-codeclimate/master/failing-codeclimate-check.png?raw=true "Failing Codeclimate Check")

## Codeclimate Analysis

Like many tools we have learned about already, `codeclimate` is configurable. So what kind of analysis Codeclimate performs depends upon what is enabled by the team.

Codeclimate configuration is stored in a `.codeclimate.yml` file that lives on root in `nitro-web`. At the time of writing, Nitro's configuration of Codeclimate runs linting on CSS files using `csslint`, Javascript files using `eslint`, and Coffeescript files using `coffeelint`. Codeclimate could also be configured to run Ruby linting with `rubocop`, but `overcommit` already takes care of this, so there is no need for duplication.

To get the full picture of what Codeclimate does and does not analyze, visit the [Codeclimate documentation](https://docs.codeclimate.com/) and review Nitro's `.codeclimate.yml`.

## Codeclimate Interface

When you encounter a Codeclimate failure, you can click directly on the notice in Github to launch a detailed breakdown. Offenses are displayed with an error messages, code snippets, line references, and additional links to explain why the code is considered a smell.

![Codeclimate Interface](https://raw.githubusercontent.com/powerhome/phrg-codeclimate/master/codeclimate-offense-interface.png?raw=true "Codeclimate Interface")

## Resources

- [Codeclimate](https://codeclimate.com/)
- [Codeclimate Documentation](https://docs.codeclimate.com/)
- [Github webhooks](https://help.github.com/articles/about-webhooks/)
- [Thoughtbot article on Codeclimate](https://thoughtbot.com/work/code_climate)
