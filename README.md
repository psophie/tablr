# Tablr

Create dynamic grids using MooTools or jQuery

## Create a simple grid

```html
<div id="areagrid"></div>
```

```javascript
// Instantiating a new grid
var grid = new Tablr("areagrid", {
    header: [
        { dataType: "number", dataIndex: "id", header: "ID" },
        { dataType: "text", dataIndex: "name", header: "Name" },
        { dataType: "text", dataIndex: "country", header: "Country" }
    ],
    height: 350,
    width: 650
});

// Filling it up
grid.setData([
    { id: 1, name: "Ana", country: "Brazil" },
    { id: 2, name: "Jack", country: "Australia" },
    { id: 3, name: "Sue", country: "England" },
    { id: 4, name: "An", country: "Japan" }
]);

// Or load via ajax
grid.loadData("source.json");
```

Here is a sample json for loading

```javascript
{
    data: [
        { id: 1, name: "Ana", country: "Brazil" },
        { id: 2, name: "Jack", country: "Australia" },
        { id: 3, name: "Sue", country: "England" },
        { id: 4, name: "An", country: "Japan" }
    ]
}
```

## License

Copyright (c) 2013 Wanderson Regis Silva, https://github.com/wregis/tablr

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>