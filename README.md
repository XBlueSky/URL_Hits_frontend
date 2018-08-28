# URL_Hits_frontend

It is the website that show the ranking of websites which most people visit and other small interesting functions.

This website implemented by Reactjs is created in 2018.July.

- [Getting Started](#getting_started) 
- [Structure](#structure)
- [Component](#component)  

## Getting_Started

> Follow the steps below, you can see the website on ```http://localhost:8001/```.

### Install
    
```console
$ npm install
```

### Run

```console
// We create proxy on `PORT 3001` and open `PORT 8001` to export outside.
$ npm start
```

## Structure

    URL_Hits_frontend/
        ├── public/             # stastic html file
        ├── src/                # app scripts and component
        ├── node_modules/       # other component we use
        └── package.json        # app npm dependencies


## Component

![Component](/img/component.png)

### < App />

> It is the start point of this website, and called by index.js.

`<Slider/>`  `<Calendar/>`  `<TabList/>`

    There are three component named <Slider/>, <Calendar/>, <TabList/> in this component.
    When user choose date by clicking Calender, we will fetch this date and send it to <TabList/>.
    
---

### < Tablist />

> It contains all of components which are core of our project.

`<Tab/>`  `<ClickData/>`

    There are two component named <Tab/>, <ClickData/> in this component.
    When user choose the one tab in Day/Week/Month, we can make component <ClickData/> to show the corresponding data.
    
---

### < ClickData />

> According to the prop data sent by component <Tablist/> and show the ranking table.

`<Table/>` `<PolyData/>` `<Routes/>`

    There are two component named <Table/>, <PolyData/>, <Routes/> in this component.
    We fetch the corresponding data from our URL_Hits_backend, and show website clicks and category in table format.
    By the way, this component can call for <PolyData/>, <Routes/> to display other function.

---

### < PolyData />

> Draw the statistic chart by one month data.

`<Popup/>` `<LineChart/>`

    There are two component named <Popup/>, <LineChart/> in this component.
    We use third party component named recharts to draw statistic chart.

---

### < Routes />

> Show the previous and next route to current websites.


