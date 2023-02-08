# U²I

U²I (Universal User Inteface) is a zero-configuration protocol for creation of simple interfaces. 

## Problem

Every time I make a power converter I need to create a small user interface for it. I usually end up with a bunch os push-buttons for on/off, reset and reference control. These quickly become insufficient and I need to overload the buttons to include more functions. 

## Solution

Split the problem into two parts: a converter which announces its API and an interface that can send and receive commands and data. A bespoke UI is created for each API. 

## Example

### Converter's API

  - [write/bool] enable output
  - [write/bool] clear fault
  - [write/f32] set reference
  - [read/{ON|OFF|FAULT}] converter state
  - [read/f32] feedback
  
## TODO/IDAS

  - Define a set of possible types
  - The converter should send some form of id/type to help the UI retain any customisations
  
  - Should there be a nested API structure to help with better UI generation?
  
