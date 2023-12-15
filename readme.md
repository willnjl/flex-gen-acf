# ACF Layout Gen

## Overview


ACF Layout Gen is command-line tool written in rust. It is designed to make the proccess creating layouts for ACF flexible content  quick and easy by automatically generating the templates and populating them with the associated fields.

It takes the  [JSON file automatically generated by ACF](https://www.advancedcustomfields.com/resources/local-json/) identifies the Flexible content field and generates template parts for the associated layouts.

The ACF Field Generator CLI is a  of generating boilerplate PHP templates from a JSON representation created by Advanced Custom Fields (ACF).

...

**Note: This tool is unofficial and not affiliated with Advanced Custom Fields (ACF)**

...

## Features

- **JSON to PHP Conversion:** Converts ACF field configurations stored in JSON format into corresponding wordpress boilerplate.
  
- **Automatic Flex Content Layouts** Create the template parts for your layouts with all the fieldsin the right place.
- **Overwrite Flag** Files will not be overwritten unless specified in the command

### Options

- `--input`: Path to the input JSON file containing ACF field configurations.
  
- `--dest`: Path where the generated code will be created.

- `--overwrite`: if true existing filse will be overwritten. false by defualt



### Usage


1. clone repository
```shell
    git clone git@github.com:willnjl/acf-layout-gen.git
```
2. install executable (Unix)
```shell
    cargo build && sudo cp target/debug/acf-layout-gen /usr/local/bin
```
3.  Run your Rust CLI app from anywhere on your machine.

```shell
   acf-layout-gen --src inc/acf-json/group_654b6e4a8a06e.json --dest template-parts/blocks 
```

### Development
```shell 
cargo watch -s 'cargo run -- --src ./data.json --dest ./blocks -o
```  

