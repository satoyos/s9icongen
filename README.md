s9icongen ・ App icon generator
===============================

## Introduction

The Ruby script `s9icongen` automatically generates icon files of all necessary sizes for iPhone and/or iPad apps (iOS 7 and above). It uses `imagemagick` and the gem `rmagick`.

## Installation

Install `imagemagick` and `rmagick` via

```bash
brew install imagemagick
gem install rmagick
```

## Usage

Just run the script 

```bash
./s9icongen.rb my_icon.png
```

The first argument is the filename of the icon image (should be quadratic and at least 1024x1024 in size). By default only iPhone icon files are generated. If one supplies a second argument (`ipad` or `universal`), iPad icon files or iPhone/iPad icon files are generated respectively.

## Rubymotion

Add the icon files to your resources directory and add the following line to your rakefile

```ruby
app.icons = Dir.glob('resources/Icon*.png').map(|icon| icon.split('/').last}
```