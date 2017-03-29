# mlrHyperopt

[![Build Status](https://travis-ci.org/jakob-r/mlrHyperopt.svg?branch=master)](https://travis-ci.org/jakob-r/mlrHyperopt)
[![Coverage Status](https://coveralls.io/repos/github/jakob-r/mlrHyperopt/badge.svg?branch=master)](https://coveralls.io/github/jakob-r/mlrHyperopt?branch=master)

Easy Hyper Parameter Optimization with [mlr](https://github.com/mlr-org/mlr/#-machine-learning-in-r) and [mlrMBO](http://mlr-org.github.io/mlrMBO/).

* [Issues and Bugs](https://github.com/jakob-r/mlrHyperopt/issues)
* [Tutorial and Documentation](https://jakob-r.github.io/mlrHyperopt)
* [Webservice](http://mlrhyperopt.jakob-r.de) (Work in Progress)
  * [Status](http://mlrhyperopt.jakob-r.de/status.php)

## Installation
```{r}
devtools::install_github("jakob-r/mlrHyperopt")
```

## Purpose
_mlrHyperopt_ aims at making hyperparameter optimization of machine learning methods super simple.
It offers tuning in one line:

```{r}
res = hyperopt(iris.task, learner = "classif.svm")
```

Mainly it uses the [learner implemented in _mlr_](http://mlr-org.github.io/mlr-tutorial/devel/html/integrated_learners/index.html) and uses the [tuning methods also available in _mlr_](http://mlr-org.github.io/mlr-tutorial/devel/html/tune/index.html).
Unfortunatly _mlr_ lacks of well defined _search spaces_ for each learner to make hyperparameter tuning easy.

_mlrHyperopt_ includes default _search spaces_ for the most common machine learning methods like _random forest_, _svm_ and _boosting_.

As the developer can not be an expert on all machine learning methods available for _R_ and _mlr_, _mlrHyperopt_ also offers a web service to share, upload and download improved _search spaces_.

## Development Status

### Web Server

*Under heavy construction*.
_ParConfigs_ are up- and downloaded via JSON and stored on the server in a database.
The very basic version is coded in PHP and available under <https://github.com/jakob-r/mlrHyperopt>.
I plan to implement everything with Ruby on Rails, including a basic user management with API-Keys.

### R package

Basic functionality works reliable. Maybe I will improve the optimization heuristics in the future.
Still *needs more default search spaces* for popular learners!

### Collaboration

Is encouraged! 👍
