# &lt;mercury-paginator&gt;

>  A Polymer element providing a solution to paginate lists (Polymer 1.0 compatible).

## Demo

[Check it live!](http://bquarks.github.io/mercury-paginator/components/mercury-paginator/)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install mercury-paginator --save
```

Or [download as ZIP](https://github.com/bquarks/mercury-paginator/archive/master.zip).

## Usage

1. Import polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import custom element:

    ```html
    <link rel="import" href="bower_components/mercury-paginator/mercury-paginator.html">
    ```

3. Start using it!

    ```html
    <template is="dom-bind">


        <mercury-paginator perpage="15" items="{{items}}"></mercury-paginator>

        <!-- Your structure data here -->
        <div class="div-table">
            <div class="head-row">
                <div class="div-cell">Id</div>
                <div class="div-cell">Item name</div>
                <div class="div-cell">Description</div>
            </div>

            <template id="items" is="dom-repeat" items="{{items}}">
                <div class="div-row">
                    <div class="div-cell">{{item.id}}</div>
                    <div class="div-cell">{{item.name}}</div>
                    <div class="div-cell">{{item.description}}</div>
                </div>
            </template>
        </div>

    </template>
    ```

## Usage

Specifies an array of elements to the component through the *items* property and set *perpage* property to a pagination number

*You can use iron-ajax element to fetch data from server.


## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1. Install [bower](http://bower.io/) & [polyserve](https://npmjs.com/polyserve):

    ```sh
    $ npm install -g bower polyserve
    ```

2. Install local dependencies:

    ```sh
    $ bower install
    ```

3. Start development server and open `http://localhost:8080/components/my-repo/`.

    ```sh
    $ polyserve
    ```

## History

For detailed changelog, check [Releases](https://github.com/jorguezz/mercury-paginator/releases).

## License

[MIT License](http://opensource.org/licenses/MIT)
