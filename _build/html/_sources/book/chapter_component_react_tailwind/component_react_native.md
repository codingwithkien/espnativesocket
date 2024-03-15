# 1.  React Native

Trong React Native, các thành phần (components) chính là các phần tử giao diện mà bạn có thể sử dụng để xây dựng ứng dụng di động. Dưới đây là một số thành phần cơ bản mà bạn thường sử dụng trong các dự án React Native:
- **View:**

   -    `View` là thành phần chính để tạo ra bố cục (layout) trong React Native.

   -    Nó tương đương với thẻ `<div>` trong HTML.
   -    `View` được sử dụng để nhóm và chứa các thành phần khác.
```js
import React from 'react';
import { View, StyleSheet } from 'react-native';

const ExampleView = () => {
  return (
    <View style={styles.container}>
      {/* Nội dung của View */}
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1, // Flex 1 để View mở rộng để điền vào không gian cha của nó
    justifyContent: 'center', // Canh giữa theo chiều dọc
    alignItems: 'center', // Canh giữa theo chiều ngang
  },
});

export default ExampleView;
```
- **Text:**
   - `Text` được sử dụng để hiển thị văn bản trong ứng dụng.

   - Tương đương với thẻ `<span>` hoặc `<p>` trong HTML.
   - Bạn có thể áp dụng các kiểu dáng và thuộc tính văn bản cho `Text`.
```js
import React from 'react';
import { Text, StyleSheet } from 'react-native';

const ExampleText = () => {
  return (
    <Text style={styles.text}>
      Hello, World!
    </Text>
  );
};

const styles = StyleSheet.create({
  text: {
    fontSize: 20,
    fontWeight: 'bold',
    color: 'blue',
  },
});

export default ExampleText;
```
- **Image**
   - `Image` cho phép hiển thị hình ảnh trong ứng dụng.

   - Tương đương với thẻ `<img>` trong HTML.

   - Bạn có thể tải hình ảnh từ nguồn cục bộ hoặc từ URL.
```js
import React from 'react';
import { Image } from 'react-native';

const ExampleImage = () => {
  return (
    <Image
      source={require('./path/to/image.png')} // đường dẫn của hình ảnh
      style={{ width: 200, height: 200 }} // kích thước của hình ảnh
    />
  );
};

export default ExampleImage;
```
- **TextInput**
   - `TextInput` là thành phần cho phép người dùng nhập văn bản.

   - Tương đương với thẻ `<input>` trong HTML.
   - Bạn có thể kiểm soát các sự kiện như việc nhập liệu hoặc thay đổi trong `TextInput`.
```js
import React, { useState } from 'react';
import { TextInput } from 'react-native';

const ExampleTextInput = () => {
  const [text, setText] = useState('');

  return (
    <TextInput
      placeholder="Enter your text here"
      onChangeText={setText} // Lấy văn bản từ TextInput
      value={text} // Gán giá trị cho TextInput
    />
  );
};

export default ExampleTextInput;
```
- **ScrollView**
   - `ScrollView` là thành phần cho phép cuộn nội dung khi nội dung vượt quá kích thước màn hình.

   - Tương đương với việc sử dụng `overflow: scroll` trong CSS.
   - `ScrollView` hữu ích khi bạn muốn hiển thị nội dung dài hoặc có thể cuộn.
```js
import React from 'react';
import { ScrollView, Text } from 'react-native';

const ExampleScrollView = () => {
  return (
    <ScrollView>
      <Text style={{ fontSize: 24 }}>Content 1</Text>
      <Text style={{ fontSize: 24 }}>Content 2</Text>
      <Text style={{ fontSize: 24 }}>Content 3</Text>
      {/* Thêm nhiều nội dung khác vào đây */}
    </ScrollView>
  );
};

export default ExampleScrollView;
```
- **TouchableOpacity**
   - `TouchableOpacity` là thành phần cho phép bạn thêm các hành động khi người dùng chạm vào nó.

   - Tương đương với việc sử dụng các sự kiện như `onClick` trong HTML.
   Khi người dùng chạm vào 
   - `TouchableOpacity`, bạn có thể thực hiện các hành động như chuyển hướng hoặc thay đổi trạng thái.
```js
import React from 'react';
import { TouchableOpacity, Text, Alert } from 'react-native';

const ExampleTouchableOpacity = () => {
  const handlePress = () => {
    Alert.alert('Button pressed!');
  };

  return (
    <TouchableOpacity onPress={handlePress}>
      <Text>Press Me</Text>
    </TouchableOpacity>
  );
};

export default ExampleTouchableOpacity;
```
- **FlatList**
   - `FlatList` là thành phần cho phép hiển thị danh sách dữ liệu có thể cuộn.

   - Tương đương với việc sử dụng `map` để render danh sách trong React.

   - `FlatList` hữu ích khi bạn cần hiển thị một danh sách lớn của các mục dữ liệu.
```js
import React from 'react';
import { FlatList, Text } from 'react-native';

const ExampleFlatList = () => {
  const data = [
    { key: 'Item 1' },
    { key: 'Item 2' },
    { key: 'Item 3' },
    // Thêm nhiều dữ liệu khác vào đây
  ];

  return (
    <FlatList
      data={data}
      renderItem={({ item }) => <Text>{item.key}</Text>}
    />
  );
};

export default ExampleFlatList;
```
- **StyleSheet**
   - `StyleSheet` là một đối tượng dùng để định nghĩa các kiểu dáng cho các thành phần giao diện.

   - Tương đương với việc sử dụng CSS để thiết lập kiểu dáng trong HTML.
   Bạn có thể sử dụng StyleSheet để tạo kiểu dáng cho các thành phần trong React Native.

Các thành phần trên là những thành phần cơ bản nhưng rất quan trọng trong việc phát triển ứng dụng React Native. Bạn có thể kết hợp chúng để xây dựng các giao diện phức tạp và linh hoạt cho ứng dụng của mình.
