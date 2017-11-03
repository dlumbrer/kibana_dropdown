# kibana_dropdown

Dropdown widget for Kibana dashboards.

Useful for embedded dashboards to provide basic filtering on specific fields.

## Installation Steps

```
cd KIBANA_HOME/plugins
git clone https://github.com/dlumbrer/kibana_dropdown.git
cd kibana_dropdown
npm install
```
> **Important:** If you have any problem with the plugin version (like a warning message "**it expected Kibana version "5.5.0", and found "5.5.x"**") only change the value of the "version" tag on the package.json to your Kibana version


#### Uninstall:
```
cd KIBANA_HOME
rm -rf plugins/kibana_dropdown/
```

![Dropdown](dropdown.png?raw=true "Dropdown Dashboard Widget")


To use this widget with analysed fields, create a keyword mapping e.g:

"speaker_name":{
  "type":"text",
  "fields": {
    "keyword": {
      "type":"keyword","ignore_above":256
    }
  }
}

To set up the dropdown widget, create a Visualisation of type 'Dropdown Picker'

![Configure Dropdown Picker](dropdownconfigure.png?raw=true "Configure Dropdown Picker")

In the visualisation options, you can set whether the dropdown is allowed to be blank. If this is true, you can hit escape while the dropdown is open to close it without selecting a value.


Licensed under the Apache License, Version 2.0

---

## development

See the [kibana contributing guide](https://github.com/elastic/kibana/blob/master/CONTRIBUTING.md) for instructions setting up your development environment.
