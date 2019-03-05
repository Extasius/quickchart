QuickChart
---

QuickChart is a service that generates images of charts from a URL.  Because these charts are simple images, they are very easy to embed in non-dynamic environments such as email, SMS, chat rooms, and so on.

## See it in action

The chart image generation service is available online at [QuickChart.io](https://quickchart.io/).  There is an interactive editor that allows you to adjust inputs and build images.

Here's an example chart that is defined completely by its URL:

![Chart from URL](https://quickchart.io/chart?c=%2F%2F%20Edit%20me!%0A%7B%0A%20%20type%3A%20%27bar%27%2C%0A%20%20data%3A%20%7B%0A%20%20%20%20labels%3A%20%5B%27January%27%2C%20%27February%27%2C%20%27March%27%2C%20%27April%27%2C%20%27May%27%5D%2C%0A%20%20%20%20datasets%3A%20%5B%7B%0A%20%20%20%20%20%20label%3A%20%27Dogs%27%2C%0A%20%20%20%20%20%20data%3A%20%5B%2050%2C%2060%2C%2070%2C%20180%2C%20190%20%5D%0A%20%20%20%20%7D%2C%20%7B%0A%20%20%20%20%20%20label%3A%20%27Cats%27%2C%0A%20%20%20%20%20%20data%3A%20%5B%20100%2C%20200%2C%20300%2C%20400%2C%20500%20%5D%0A%20%20%20%20%7D%5D%0A%20%20%7D%0A%7D)

The above image can be included anywhere you like.  Here is its URL:

[https://quickchart.io/chart?c={type:'bar',data:{labels:['January','February','March','April','May'],datasets:[{label:'Dogs',data:[50,60,70,180,190]},{label:'Cats',data:[100,200,300,400,500]}]}}](https://quickchart.io/chart?c={type:'bar',data:{labels:['January','February','March','April','May'],datasets:[{label:'Dogs',data:[50,60,70,180,190]},{label:'Cats',data:[100,200,300,400,500]}]}})

As you can see, the URL itself defines the chart:

```
{
  type: 'bar',
  data: {
    labels: ['January', 'February', 'March', 'April', 'May'],
    datasets: [{
      label: 'Dogs',
      data: [ 50, 60, 70, 180, 190 ]
    }, {
      label: 'Cats',
      data: [ 100, 200, 300, 400, 500 ]
    }]
  }
}
```

## Dependencies and Installation

Chart generation requires several system dependencies: Cairo, Pango, libjpeg, and libgif.  Run `./scripts/setup.sh` for a fresh install on Linux machines (note that this also installs yarn and node).  

To install system dependencies on Mac OSX, you probably just need to `brew install cairo`.

Once you have system dependencies installed, run `yarn install` or `npm install` to install the node dependencies.

## Running the server

`node index.js` will start the server on port 3400.

## License

QuickChart is open source, licensed under version 3 of the GNU GPL.  If you would like to use this project for commercial purposes, please [contact me](https://www.ianww.com/).