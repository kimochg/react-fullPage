## Why another react-fullPage?
* Simpler & Smaller
* ES6
* Follow ESlint (Airbnb)
* Adapt to our [generator-modation](https://github.com/zhaozhiming/generator-modation) (It's a comfortable react-redux generator)

## Install

`npm install react-scrollpage`

## Usage

```
import { ScrollPage, Section } from 'react-scrollpage';

class Foo extends Component {
  render() {
    return (
      <ScrollPage
        curPage={1}
        totalPage={4}
      >
        <Section>
          Page1
        </Section>
        <Section>
          Page2
        </Section>
        <Section>
          Page3
        </Section>
        <Section>
          Page4
        </Section>
      </ScrollPage>
    )
  }
}

var app = document.getElementById('app');
ReactDOM.render(<Foo />, app);
```


## Example

```
npm install

cd ./example
webpack

// That's it! Open example/index.html directly.
```

## API
```
window.turnTo(number);

// 0 < number <= totalPage

```
If `number < 0 || number > totalPage` , it will not print any error but keep scrolling to target position. `transform to window.innerHeight * number`