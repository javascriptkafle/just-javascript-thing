# ways to create React components:

### 1 : Function ("stateless") components
```
    const FirstComponent = props => (
        <div> {props.content} </div>
    )
```

### 2 : Using React.createClass()
```
    const SecondComponent = React.createClass({
        render : function() {
            return (
                <div> {this.props.content} </div>
            );
        }
    });
```

### 3 : Using ES2015 Classes
```
    class ThirdComponent extends React.Component{
        render(){
            return(
                <div> {this.props.content} </div>
            );
        }
    }
```

# passing props to these components

```
    const ParentComponent = function(props) {
        const someText = "FooBar";
        return(
            <FirstComponent content={someText} />
            <SecondComponent content={someText} />
            <ThirdComponent content={someText} /> 
        );
    }
```