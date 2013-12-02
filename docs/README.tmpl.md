# {%= name %} [![NPM version](https://badge.fury.io/js/{%= name %}.png)](http://badge.fury.io/js/{%= name %}) {% if (travis) { %} [![Build Status]({%= travis %}.png)]({%= travis %}){% } %}

> {%= description %}

## Getting Started

{%= _.doc("getting-started.md") %}

## Options

{%= _.doc("options.md") %}

## Usage Examples

{%= _.doc("examples-*.md") %}

## Contributing

Please see the [Contributing to Assemble](http://assemble.io/contributing) guide for information on contributing to this project.

## Authors

**Jon Schlinkert**

+ [http://twitter.com/jonschlinkert](http://twitter.com/jonschlinkert)
+ [http://github.com/jonschlinkert](http://github.com/jonschlinkert)

**Hariadi Hinta**

+ [http://twitter.com/hariadi](http://twitter.com/hariadi)
+ [http://github.com/hariadi](http://github.com/hariadi)

## Release History
{% if (changelog) {
  _.each(changelog, function(details, version) {
    var date = details.date;
    if (date instanceof Date) {
      date = grunt.template.date(new Date(date.getTime() + date.getTimezoneOffset() * 60000), 'yyyy-mm-dd');
    }
    print('\n * ' + [
      date,
      version,
      details.changes.join(' '),
    ].join('\u2003\u2003\u2003'));
  });
} else { %}
_(Nothing yet)_
{% } %}

## License
[MIT License](LICENSE-MIT)

***

_This file was generated on {%= grunt.template.today() %}._