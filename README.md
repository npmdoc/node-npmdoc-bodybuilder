# api documentation for  [bodybuilder (v2.1.0)](https://github.com/danpaz/bodybuilder#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-bodybuilder.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bodybuilder) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bodybuilder.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bodybuilder)
#### An elasticsearch query body builder.

[![NPM](https://nodei.co/npm/bodybuilder.png?downloads=true)](https://www.npmjs.com/package/bodybuilder)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-bodybuilder_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-bodybuilder/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Daniel Paz-Soldan",
        "email": "daniel.pazsoldan@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/danpaz/bodybuilder/issues"
    },
    "contributors": [
        {
            "name": "Nicolás Fantone"
        },
        {
            "name": "Nauval Atmaja"
        },
        {
            "name": "Ferron Hanse"
        },
        {
            "name": "Dave Cranwell"
        },
        {
            "name": "Anton Samper Rivaya"
        }
    ],
    "dependencies": {
        "lodash": "4.9.0"
    },
    "description": "An elasticsearch query body builder.",
    "devDependencies": {
        "babel-cli": "6.5.1",
        "babel-core": "6.5.1",
        "babel-plugin-lodash": "2.0.1",
        "babel-preset-es2015": "6.5.0",
        "babel-register": "6.18.0",
        "babel-tape-runner": "2.0.1",
        "documentation": "4.0.0-beta10",
        "eslint": "1.10.2",
        "tap-spec": "4.1.1",
        "tape": "4.6.2",
        "tape-watch": "2.2.4",
        "webpack": "1.12.13"
    },
    "directories": {},
    "dist": {
        "shasum": "45bd98566d13848ba6f50a1eeeb1c10273b216a8",
        "tarball": "https://registry.npmjs.org/bodybuilder/-/bodybuilder-2.1.0.tgz"
    },
    "files": [
        "browser/",
        "lib/",
        "src/",
        "repl.js"
    ],
    "gitHead": "0bf3cc4f3bdb6f8f301c87c9978eb8ef5d9592c0",
    "homepage": "https://github.com/danpaz/bodybuilder#readme",
    "keywords": [
        "elasticsearch",
        "bodybuilder",
        "querying",
        "queries",
        "query",
        "elastic",
        "search",
        "dsl"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "danpaz",
            "email": "daniel.pazsoldan@gmail.com"
        }
    ],
    "name": "bodybuilder",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/danpaz/bodybuilder.git"
    },
    "scripts": {
        "build": "npm run build:babel && npm run build:umd && npm run build:docs",
        "build:babel": "babel src --out-dir lib",
        "build:docs": "documentation build src/index.js -o docs -f html --name bodybuilder",
        "build:umd": "webpack lib browser/bodybuilder.min.js",
        "check": "npm run lint && npm test",
        "git-commit": "git add docs browser && git commit -m \"Commit built files\"",
        "git-push": "git push origin master && git push origin v$npm_package_version",
        "lint": "eslint src test",
        "postversion": "npm run git-push",
        "preversion": "npm run check && npm run build && npm run git-commit",
        "style": "npm run lint",
        "test": "babel-tape-runner test/* | tap-spec",
        "watch:test": "tape-watch test/* -r babel-register -p tap-spec"
    },
    "version": "2.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module bodybuilder](#apidoc.module.bodybuilder)
1.  object <span class="apidocSignatureSpan">bodybuilder.</span>aggregation_builder
1.  object <span class="apidocSignatureSpan">bodybuilder.</span>bool_query
1.  object <span class="apidocSignatureSpan">bodybuilder.</span>filter_builder
1.  object <span class="apidocSignatureSpan">bodybuilder.</span>query_builder
1.  object <span class="apidocSignatureSpan">bodybuilder.</span>utils

#### [module bodybuilder.aggregation_builder](#apidoc.module.bodybuilder.aggregation_builder)
1.  [function <span class="apidocSignatureSpan">bodybuilder.aggregation_builder.</span>default ()](#apidoc.element.bodybuilder.aggregation_builder.default)

#### [module bodybuilder.bool_query](#apidoc.module.bodybuilder.bool_query)
1.  [function <span class="apidocSignatureSpan">bodybuilder.bool_query.</span>default (condition, query)](#apidoc.element.bodybuilder.bool_query.default)

#### [module bodybuilder.filter_builder](#apidoc.module.bodybuilder.filter_builder)
1.  [function <span class="apidocSignatureSpan">bodybuilder.filter_builder.</span>default ()](#apidoc.element.bodybuilder.filter_builder.default)

#### [module bodybuilder.query_builder](#apidoc.module.bodybuilder.query_builder)
1.  [function <span class="apidocSignatureSpan">bodybuilder.query_builder.</span>default ()](#apidoc.element.bodybuilder.query_builder.default)

#### [module bodybuilder.utils](#apidoc.module.bodybuilder.utils)
1.  [function <span class="apidocSignatureSpan">bodybuilder.utils.</span>boolMerge (newObj, currentObj)](#apidoc.element.bodybuilder.utils.boolMerge)
1.  [function <span class="apidocSignatureSpan">bodybuilder.utils.</span>buildClause (field, value, opts)](#apidoc.element.bodybuilder.utils.buildClause)
1.  [function <span class="apidocSignatureSpan">bodybuilder.utils.</span>mergeConcat ()](#apidoc.element.bodybuilder.utils.mergeConcat)
1.  [function <span class="apidocSignatureSpan">bodybuilder.utils.</span>sortMerge (current, field, value)](#apidoc.element.bodybuilder.utils.sortMerge)



# <a name="apidoc.module.bodybuilder"></a>[module bodybuilder](#apidoc.module.bodybuilder)



# <a name="apidoc.module.bodybuilder.aggregation_builder"></a>[module bodybuilder.aggregation_builder](#apidoc.module.bodybuilder.aggregation_builder)

#### <a name="apidoc.element.bodybuilder.aggregation_builder.default"></a>[function <span class="apidocSignatureSpan">bodybuilder.aggregation_builder.</span>default ()](#apidoc.element.bodybuilder.aggregation_builder.default)
- description and source-code
```javascript
function aggregationBuilder() {
  var aggregations = {};

  function makeAggregation(type, field) {
    for (var _len = arguments.length, args = Array(_len > 2 ? _len - 2 : 0), _key = 2; _key < _len; _key++) {
      args[_key - 2] = arguments[_key];
    }

    var aggName = (0, _find2.default)(args, _isString2.default) || 'agg_' + type + '_' + field;
    var opts = (0, _find2.default)(args, _isPlainObject2.default);
    var nested = (0, _find2.default)(args, _isFunction2.default);
    var nestedClause = {};

    if ((0, _isFunction2.default)(nested)) {
      var nestedResult = nested(Object.assign({}, aggregationBuilder(), (0, _filterBuilder2.default)()));
      if (nestedResult.hasFilter()) {
        nestedClause.filter = nestedResult.getFilter();
      }
      if (nestedResult.hasAggregations()) {
        nestedClause.aggs = nestedResult.getAggregations();
      }
    }

    var innerClause = Object.assign({}, _defineProperty({}, type, (0, _utils.buildClause)(field, null, opts)), nestedClause);

    Object.assign(aggregations, _defineProperty({}, aggName, innerClause));
  }

  return {
<span class="apidocCodeCommentSpan">    /**
     * Add an aggregation clause to the query body.
     *
     * @param  {string|Object} type      Name of the aggregation type, such as
     *                                   ''sum'' or ''terms''.
     * @param  {string}        field     Name of the field to aggregate over.
     * @param  {Object}        [options] (optional) Additional options to
     *                                   include in the aggregation.
     * @param  {string}        [name]    (optional) A custom name for the
     *                                   aggregation, defaults to
     *                                   'agg_<type>_<field>'.
     * @param  {Function}      [nest]    (optional) A function used to define
     *                                   sub-aggregations as children. This
     *                                   _must_ be the last argument.
     *
     * @return {bodybuilder} Builder.
     *
     * @example
     * bodybuilder()
     *   .aggregation('max', 'price')
     *   .build()
     *
     * bodybuilder()
     *   .aggregation('percentiles', 'load_time', {
     *     percents: [95, 99, 99.9]
     *   })
     *   .build()
     *
     * bodybuilder()
     *   .aggregation('date_range', 'date', {
     *     format: 'MM-yyy',
     *     ranges: [{ to: 'now-10M/M' }, { from: 'now-10M/M' }]
     *   })
     *   .build()
     *
     * bodybuilder()
     *   .aggregation('diversified_sampler', 'user.id', { shard_size: 200 }, (a) => {
     *     return a.aggregation('significant_terms', 'text', 'keywords')
     *   })
     *   .build()
     */
</span>    aggregation: function aggregation() {
      makeAggregation.apply(undefined, arguments);
      return this;
    },


    /**
     * Alias for 'aggregation'.
     *
     * @return {bodybuilder} Builder.
     */
    agg: function agg() {
      return this.aggregation.apply(this, arguments);
    },
    getAggregations: function getAggregations() {
      return aggregations;
    },
    hasAggregations: function hasAggregations() {
      return !!(0, _size2.default)(aggregations);
    }
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bodybuilder.bool_query"></a>[module bodybuilder.bool_query](#apidoc.module.bodybuilder.bool_query)

#### <a name="apidoc.element.bodybuilder.bool_query.default"></a>[function <span class="apidocSignatureSpan">bodybuilder.bool_query.</span>default (condition, query)](#apidoc.element.bodybuilder.bool_query.default)
- description and source-code
```javascript
function boolQuery(condition, query) {
  var cond = CONDITIONS_MAP[condition];
  return {
    bool: _defineProperty({}, cond, [query])
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bodybuilder.filter_builder"></a>[module bodybuilder.filter_builder](#apidoc.module.bodybuilder.filter_builder)

#### <a name="apidoc.element.bodybuilder.filter_builder.default"></a>[function <span class="apidocSignatureSpan">bodybuilder.filter_builder.</span>default ()](#apidoc.element.bodybuilder.filter_builder.default)
- description and source-code
```javascript
function filterBuilder() {
  var filter = {};

  function addMinimumShouldMatch(str) {
    var shouldClause = (0, _get2.default)(filter, 'bool.should');
    if (shouldClause && shouldClause.length > 1) {
      filter.bool['minimum_should_match'] = str;
    }
  }

  function makeFilter(boolType, filterType) {
    var nested = {};

    for (var _len = arguments.length, args = Array(_len > 2 ? _len - 2 : 0), _key = 2; _key < _len; _key++) {
      args[_key - 2] = arguments[_key];
    }

    if ((0, _isFunction2.default)((0, _last2.default)(args))) {
      var nestedCallback = args.pop();
      var nestedResult = nestedCallback(Object.assign({}, (0, _queryBuilder2.default)(), filterBuilder(), (0, _aggregationBuilder2
.default)()));
      if (nestedResult.hasQuery()) {
        nested.query = nestedResult.getQuery();
      }
      if (nestedResult.hasFilter()) {
        nested.filter = nestedResult.getFilter();
      }
      if (nestedResult.hasAggregations()) {
        nested.aggs = nestedResult.getAggregations();
      }
    }

    filter = (0, _utils.boolMerge)(_defineProperty({}, filterType, Object.assign(_utils.buildClause.apply(undefined, args), nested
)), filter, boolType);
  }

  return {
<span class="apidocCodeCommentSpan">    /**
     * Add a filter clause to the query body.
     *
     * @param  {string}        type    Filter type.
     * @param  {string|Object} field   Field to filter or complete filter
     *                                 clause.
     * @param  {string|Object} value   Filter term or inner clause.
     * @param  {Object}        options (optional) Additional options for the
     *                                 filter clause.
     * @param  {Function}      [nest]  (optional) A function used to define
     *                                 sub-filters as children. This _must_ be
     *                                 the last argument.
     *
     * @return {bodybuilder} Builder.
     *
     * @example
     * bodybuilder()
     *   .filter('term', 'user', 'kimchy')
     *   .build()
     */
</span>    filter: function filter() {
      for (var _len2 = arguments.length, args = Array(_len2), _key2 = 0; _key2 < _len2; _key2++) {
        args[_key2] = arguments[_key2];
      }

      makeFilter.apply(undefined, ['and'].concat(args));
      return this;
    },


    /**
     * Alias for 'filter'.
     *
     * @return {bodybuilder} Builder.
     */
    andFilter: function andFilter() {
      return this.filter.apply(this, arguments);
    },


    /**
     * Alias for 'filter'.
     *
     * @return {bodybuilder} Builder.
     */
    addFilter: function addFilter() {
      return this.filter.apply(this, arguments);
    },


    /**
     * Add a "should" filter to the query body.
     *
     * Same arguments as 'filter'.
     *
     * @return {bodybuilder} Builder.
     */
    orFilter: function orFilter() {
      for (var _len3 = arguments.length, args = Array(_len3), _key3 = 0; _key3 < _len3; _key3++) {
        args[_key3] = arguments[_key3];
      }

      makeFilter.apply(undefined, ['or'].concat(args));
      return this;
    },


    /**
     * Add a "must_not" filter to the query body.
     *
     * Same arguments as 'filter'.
     *
     * @return {bodybuilder} Builder.
     */
    notFilter: function notFilter() {
      for (var _len4 = arguments.length, args = Array(_len4), _key4 = 0; _key4 < _len4; _key4++) {
        args[_key4] = arguments[_key4];
      }

      makeFilter.apply(undefined, ['not'].concat(args));
      return this;
    },


    /**
     * Set the 'minimum_should_match' property on a bool filter with more than
     * one 'should' clause.
     *
     * @param  {any} param  minimum_should_match parameter. For possible values
     *                      see https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html
     * @return {bodybuilder} Builder.
     */
    filterMinimumShouldMatch: function filterMinimumShouldMatch(param) {
      addMinimumShouldMatch(param);
      return this;
    },
    getFilter: function getFilter() {
      return filter;
    },
    hasFilter: function h ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bodybuilder.query_builder"></a>[module bodybuilder.query_builder](#apidoc.module.bodybuilder.query_builder)

#### <a name="apidoc.element.bodybuilder.query_builder.default"></a>[function <span class="apidocSignatureSpan">bodybuilder.query_builder.</span>default ()](#apidoc.element.bodybuilder.query_builder.default)
- description and source-code
```javascript
function queryBuilder() {
  var query = {};

  function addMinimumShouldMatch(str) {
    var shouldClause = (0, _get2.default)(query, 'bool.should');
    if (shouldClause && shouldClause.length > 1) {
      query.bool['minimum_should_match'] = str;
    }
  }

  function makeQuery(boolType, queryType) {
    var nested = {};

    for (var _len = arguments.length, args = Array(_len > 2 ? _len - 2 : 0), _key = 2; _key < _len; _key++) {
      args[_key - 2] = arguments[_key];
    }

    if ((0, _isFunction2.default)((0, _last2.default)(args))) {
      var nestedCallback = args.pop();
      var nestedResult = nestedCallback(Object.assign({}, queryBuilder(), (0, _filterBuilder2.default)()));
      if (nestedResult.hasQuery()) {
        nested.query = nestedResult.getQuery();
      }
      if (nestedResult.hasFilter()) {
        nested.filter = nestedResult.getFilter();
      }
    }

    query = (0, _utils.boolMerge)(_defineProperty({}, queryType, Object.assign(_utils.buildClause.apply(undefined, args), nested
)), query, boolType);
  }

  return {
<span class="apidocCodeCommentSpan">    /**
     * Add a query clause to the query body.
     *
     * @param  {string}        type    Query type.
     * @param  {string|Object} field   Field to query or complete query clause.
     * @param  {string|Object} value   Query term or inner clause.
     * @param  {Object}        options (optional) Additional options for the
     *                                 query clause.
     * @param  {Function}      [nest]  (optional) A function used to define
     *                                 sub-filters as children. This _must_ be
     *                                 the last argument.
     *
     * @return {bodybuilder} Builder.
     *
     * @example
     * bodybuilder()
     *   .query('match_all')
     *   .build()
     *
     * bodybuilder()
     *   .query('match_all', { boost: 1.2 })
     *   .build()
     *
     * bodybuilder()
     *   .query('match', 'message', 'this is a test')
     *   .build()
     *
     * bodybuilder()
     *   .query('terms', 'user', ['kimchy', 'elastic'])
     *   .build()
     *
     * bodybuilder()
     *   .query('nested', { path: 'obj1', score_mode: 'avg' }, (q) => {
     *     return q
     *       .query('match', 'obj1.name', 'blue')
     *       .query('range', 'obj1.count', {gt: 5})
     *   })
     *   .build()
     */
</span>    query: function query() {
      for (var _len2 = arguments.length, args = Array(_len2), _key2 = 0; _key2 < _len2; _key2++) {
        args[_key2] = arguments[_key2];
      }

      makeQuery.apply(undefined, ['and'].concat(args));
      return this;
    },


    /**
     * Alias for 'query'.
     *
     * @return {bodybuilder} Builder.
     */
    andQuery: function andQuery() {
      return this.query.apply(this, arguments);
    },


    /**
     * Alias for 'query'.
     *
     * @return {bodybuilder} Builder.
     */
    addQuery: function addQuery() {
      return this.query.apply(this, arguments);
    },


    /**
     * Add a "should" query to the query body.
     *
     * Same arguments as 'query'.
     *
     * @return {bodybuilder} Builder.
     */
    orQuery: function orQuery() {
      for (var _len3 = arguments.length, args = Array(_len3), _key3 = 0; _key3 < _len3; _key3++) {
        args[_key3] = arguments[_key3];
      }

      makeQuery.apply(undefined, ['or'].concat(args));
      return this;
    },


    /**
     * Add a "must_not" query to the query body.
     *
     * Same arguments as 'query'.
     *
     * @return {bodybuilder} Builder.
     */
    notQuery: function notQuery() {
      for (var _len4 = arguments.length, args = Array(_len4), _key4 = 0; _key4 < _len4; _key4++) {
        args[_key4] = arguments[_key4];
      }

      makeQuery.apply(undefined, ['not'].concat(args));
      return this;
    },


    /**
     * Set the 'minimum_should_match' property on a bool query with more than
     * one 'should' clause.
     *
     * @param  {any} param  minimum_should_match parameter. For possible values
     *                      see https://www.elastic.co/guide/en/elasticsearch/reference/curre ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bodybuilder.utils"></a>[module bodybuilder.utils](#apidoc.module.bodybuilder.utils)

#### <a name="apidoc.element.bodybuilder.utils.boolMerge"></a>[function <span class="apidocSignatureSpan">bodybuilder.utils.</span>boolMerge (newObj, currentObj)](#apidoc.element.bodybuilder.utils.boolMerge)
- description and source-code
```javascript
function boolMerge(newObj, currentObj) {
  var boolType = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : 'and';

  var boolCurrent = void 0;
  var boolNew = void 0;

  // Only one, no need for bool.
  if ((0, _isEmpty2.default)(currentObj)) {
    // Allow starting with 'or' and 'not' queries.
    if (boolType !== 'and') {
      return (0, _boolQuery2.default)(boolType, newObj);
    }
    return newObj;
  }

  // Make bools out of the new and existing filters.
  boolCurrent = currentObj.bool ? currentObj : (0, _boolQuery2.default)('must', currentObj);
  boolNew = newObj.bool ? newObj : (0, _boolQuery2.default)(boolType, newObj);

  return mergeConcat({}, boolCurrent, boolNew);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bodybuilder.utils.buildClause"></a>[function <span class="apidocSignatureSpan">bodybuilder.utils.</span>buildClause (field, value, opts)](#apidoc.element.bodybuilder.utils.buildClause)
- description and source-code
```javascript
function buildClause(field, value, opts) {
  var hasField = !(0, _isNil2.default)(field);
  var hasValue = !(0, _isNil2.default)(value);
  var mainClause = {};

  if (hasValue) {
    mainClause = _defineProperty({}, field, value);
  } else if ((0, _isObject2.default)(field)) {
    mainClause = field;
  } else if (hasField) {
    mainClause = { field: field };
  }

  return Object.assign({}, mainClause, opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bodybuilder.utils.mergeConcat"></a>[function <span class="apidocSignatureSpan">bodybuilder.utils.</span>mergeConcat ()](#apidoc.element.bodybuilder.utils.mergeConcat)
- description and source-code
```javascript
function mergeConcat() {
  var args = Array.prototype.slice.call(arguments, 0);
  args.push(function customizer(a, b) {
    if ((0, _isPlainObject2.default)(a)) {
      return (0, _assignWith2.default)(a, b, customizer);
    } else if ((0, _isArray2.default)(a)) {
      return a.concat(b);
    } else {
      return b;
    }
  });
  return _assignWith2.default.apply(null, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bodybuilder.utils.sortMerge"></a>[function <span class="apidocSignatureSpan">bodybuilder.utils.</span>sortMerge (current, field, value)](#apidoc.element.bodybuilder.utils.sortMerge)
- description and source-code
```javascript
function sortMerge(current, field, value) {
  var payload = void 0;

  if ((0, _isPlainObject2.default)(value)) {
    payload = _defineProperty({}, field, (0, _assign2.default)({}, value));
  } else {
    payload = _defineProperty({}, field, { order: value });
  }

  var idx = (0, _findIndex2.default)(current, function (o) {
    return o[field] != undefined;
  });

  if (idx == -1) {
    current.push(payload);
  } else {
    (0, _extend2.default)(current[idx], payload);
  }

  return current;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
