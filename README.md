# Redmine Custom Reports Plugin (with charts)

Redmine plugin to create project reports using [d3.js](http://d3js.org/) charts (with using [NVD3](http://nvd3.org/)). The data for the report - the number of filtered issues grouped by a column.

You can use multiple data series. Issues filtered by ordinary redmine filters.

Tickets are grouped together on the same field, on how tickets can be grouped in a query. Additionally, you can group tickets by text custom fields. In addition to regular columns, you can use custom fields with type "text" to group.

## Permissions

There are public and private custom reports. Permission "View custom reports" allows user to view public and private reports. Permission "Manage custom reports" allows user to manage their (private) reports. And last permission "Manage public custom reports" allows user to manage public reports.

## Installing a plugin

1. Copy plugin directory into #{RAILS_ROOT}/plugins.
If you are downloading the plugin directly from GitHub,
you can do so by changing into your plugin directory and issuing a command like

        git clone https://github.com/CtrlMajSup/redmine_custom_reports.git

2. Run the following command to upgrade your database (make a db backup before).

        bundle exec rake redmine:plugins:migrate RAILS_ENV=production

3. Restart Redmine

4. Go to one of your project settings. Click on the Modules tab.
You should see the "Custom reports" module at the end of the modules list.
Enable plugin at project level. Now you will see "Custom report" tab at the project menu.

## Screenshot

![Sample](screenshot.png)

## Compatibility

This version supports redmine 5.x (tested on 5.0.5)

For all tested versions see the "tests matrix":https://travis-ci.org/Restream/redmine_custom_reports
