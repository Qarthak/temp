# Plugin for Introductory Programming Courses

## Introduction

This is a C++ library for teaching basic concepts in CSF111 Computer Programming. It's currently mostly a wrapper around the Standard Library so there's lots of room for improvement. We've also developed a VSCode extension to provide functionality like: fetch, switch assignment, change git user, submit, delete, auto commit and active time logging on save

## Project Ideas

Here's 3 broad areas we could work on to improve the plugin

1) Improving the library: Adding features, like a simple GUI, or detailed logs for better debugging or just refactoring the code
2) Improving the plugin: We faced a lot of issues with docker and git. We could redesign the toolchain to be easier to use, maybe replace docker with a simpler alternative. This option is pretty open ended and any input is welcome
3) Analysis on the date: Around 90 students signed the consent form to let us use their data. We could anonymize the data and publish a paper like this one: [Research Paper](https://arxiv.org/abs/2012.05085)

### Prerequisites

Experience with basics of C++. We can teach you about libraries and linking but we can't teach C++ from scratch. It's a big plus if you were one of the students who used this library and have ideas on how to improve it. 

## Current Structure (WIP)

Everything is under `namespace cp`. No nested namespaces.

* io.hxx
  * `void print(int)` and `void println(int)`, similarly for double, bool, char, cp::string
  * `void println()`
  * `int read_int()`, similarly for double, bool, char, cp::string
* fileio.hxx: two classes `input_file` and `output_file`
  * methods common to both
    * ctor with a `cp::string` param: name of the file
    * `bool eof()`
    * `bool is_open()`
    * `void close()`
    * `cp::string name()`
  * methods for input_file
    * `int read_int()`, similarly for double, bool, char, cp::string
  * methods for output_file
    * `void print(int)` and `void println(int)`, similarly for double, bool, char, cp::string
    * `void println()`
* math.hxx
  * `double sqrt(double)`
  * `double ceiling(double)`
  * `double floor(double)`
  * `int abs(int)`, also for `double`
  * `inline constexpr double e`
  * `inline constexpr double pi`
* logical.hxx
  * `bool and(bool, bool)`
  * `bool or(bool, bool)`
  * `bool not(bool)`
* string.hxx
  * ctor, dtor, operator=
  * `operator[]`
  * `operator==`, `operator<=>`
  * `operator+`
  * `operator>>`, `operator<<`
  * `size_type length()`
  * `to_string(int)` similarly for double, bool, char
  * `int to_int()` similarly for double, bool, char
  * iterators `begin` and `end`
  * `int index_of(char)`
  * `void clear()`
  * `inline constexpr cp::string newline`
* list.hxx - `list<T>` that internally uses `vector<T>` and provides following methods
  * ctor, dtor, operator=
  * iterators `begin`, `end`
  * `size_type size()`
  * `void clear()`
  * `void insert_at(size_type pos, int value)`
  * `int remove_from(size_type pos)`
  * `operator==`, `operator<=>`
  * `cp::string to_string()`
  * To hide templates, use `typedef list_int list<int>`, similarly for double, bool, char, cp::string
  * To hide templates, use `typedef list_int list<int>`, similarly for double, bool, char, cp::string
* assert.hxx
  * `void assert(bool)`, `void assert(bool, cp::string)`

## Mentors

- [Sarthak Chaudhary](https://github.com/qarthak)
- [Tanmay Devale](https://github.com/tanmaydevale)
- [Satchit Hari](https://github.com/satchit1910)
- [Mrudul M Nair](https://github.com/mrudul2019)