# 智能提示

- order: 5

输入框自动完成功能，下面是一个账号注册表单的例子。

---


````jsx
let Select = require('uxcore-select2');
let Option = Select.Option;

let Test = React.createClass({
  getInitialState() {
    return {
      options: []
    };
  },
  handleChange(value) {
    var options;
    if (!value || value.indexOf('@') >= 0) {
      options = [];
    } else {
      options = ['gmail.com', '163.com', 'qq.com'].map(function(domain) {
        var email = value + '@' + domain;
        return <Option key={email}>{email}</Option>;
      });
    }
    this.setState({
      options: options
    });
  },
  render() {
    return <Select combobox
      style={{width:200}}
      onChange={this.handleChange}
      searchPlaceholder="请输入账户名">
      {this.state.options}
    </Select>;
  }
});

ReactDOM.render(<Test />, document.getElementById('components-select2-demo-combobox'));
````
