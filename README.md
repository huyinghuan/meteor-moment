# Moment v2.6.0 for Meteor

[Moment.js](http://momentjs.com/), a JavaScript date library for parsing, validating, manipulating, and formatting dates, packaged for Meteor.

Installation
-------------
```
cd meteor-application
mkdir packages && cd packages
git clone https://github.com/huyinghuan/meteor-moment.git moment
cd ..
meteor add moment
```

Usage
-------------
in client or server js ,just like the [moment docs](http://momentjs.com/docs/) tell you:

`var oneMomentPlease = moment();`

Helper
-------------
In the template, format date to string. Html:

```
{{moment time_number 'YYYY-MM-DD HH:mm:ss'}}
{{moment time_date 'YYYY-MM-DD HH:mm:ss'}}
```
the first paramet is a number of  milliseconds since the Unix Epoch (Jan 1 1970 12AM UTC) or a Date type. for example:

```
Template.hello.time_number = function () {
  return new Date().getTime();
};

Template.hello.time_date = function(){
  return new Date();
}
```

Helper Test
-------------
https://github.com/huyinghuan/test-meteor-moment