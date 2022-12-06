# Vue Notes

### Course: [Vuejs Fast Crash Course](https://www.udemy.com/course/vuejs-fast-crash-course/)
### Beautiful images of codes: [Carbon](https://carbon.now.sh/)

### Index Html

![index](https://user-images.githubusercontent.com/46112568/205897404-94c08614-7159-47ba-aa38-372ed1c6a21f.png)

- Directly used vue with the script src=https://cdn.jsdelivr.net/npm/vue/dist/vue.js
- Created a new Vue in script tag with element app and a datum message with value Hello. Then in div with tag app, displayed message in curvy brackets {{}}

### String Interpolation

![string_interpolation](https://user-images.githubusercontent.com/46112568/205897955-c6f52aa5-5503-4550-905a-aeab520c0961.png)

- Created new variables, changed them through console, implemented a basic if else statement, split reverse joined a string value.

### Data Binding

![data_binding](https://user-images.githubusercontent.com/46112568/205898446-d4529545-b81a-4885-9915-13d6221bf2da.png)

- Created a url string value, binded it to href using v-bind. For short of v-bind:href you can type :href as well.

### Twoway Binding

![twoway_binding](https://user-images.githubusercontent.com/46112568/205898649-356d970c-6568-4e34-be04-56310baea567.png)

![twoway_binding_result](https://user-images.githubusercontent.com/46112568/205898702-eb0bfc12-cfba-43f8-b090-93c1b4a45f35.png)

### Twoway Databinding 

![twoway_databinding](https://user-images.githubusercontent.com/46112568/205898877-0fb0bb29-039a-45c5-ac01-9ad5303bd373.png)

![twoway_databinding_result](https://user-images.githubusercontent.com/46112568/205898928-bfbf855e-92d5-4084-961a-93d91bc4daed.png)

### Directives

![directives](https://user-images.githubusercontent.com/46112568/205899218-9326b42e-ff62-40cf-a495-f8f8feeec205.png)

- v-on:click and @click are the same.
- Submit.prevent was used to stop refreshing the page after clicking submit button.

### Inline Style Binding

![inline_style_binding](https://user-images.githubusercontent.com/46112568/205899493-fe2b3ffc-a567-4a02-a2ee-83408dae2ccc.png)

![inline_style_binding_result](https://user-images.githubusercontent.com/46112568/205899520-24587ca6-7b4b-4ffa-8bac-aab6d8db5e70.png)


### Event Binding

![event_binding](https://user-images.githubusercontent.com/46112568/205899824-d623de3c-c62a-4a94-b75b-cf76e1b2b9ee.png)

- this. is used to access the values in the current Vue app.
- When Increase is clicked fontSize will increase by 1 px,
  - ![increase](https://user-images.githubusercontent.com/46112568/205899866-7318e233-3c9f-4e1f-9583-58922addf7e1.png)
- When Decrease is clicked fontSize will decrease by 1px.
  - ![decrease](https://user-images.githubusercontent.com/46112568/205899899-121c756c-2f39-4011-aed2-ec44e0975d81.png)

### Conditional Rendering

![conditional_rendering](https://user-images.githubusercontent.com/46112568/205900058-81c1a7fe-92d7-45c4-8a34-56243036f2e8.png)

![conditional_rendering_result](https://user-images.githubusercontent.com/46112568/205900095-aeecb36e-4a3a-4d4a-9e9d-13915af8150f.png)

### List Rendering

![list_rendering](https://user-images.githubusercontent.com/46112568/205900340-5b2c893a-6e73-45f9-833d-9cbfd6db8711.png)

- v-for="post in posts" :key="post.id"
 - ![list_rendering_result](https://user-images.githubusercontent.com/46112568/205900425-aa2f374a-a61e-4f44-bbf2-6ccbfa7460f0.png)

### Computed Properties

![computed_properties](https://user-images.githubusercontent.com/46112568/205900575-d3e94f79-e026-410c-876f-41084644182b.png)

### Watchers

![watchers](https://user-images.githubusercontent.com/46112568/205900944-635e7aa3-062d-42a0-a742-f51f01acb297.png)

### Registering Components

![registering_components](https://user-images.githubusercontent.com/46112568/205901064-0c76787c-659b-4e14-9ba4-8a386f27b23a.png)

### Inline Template

![inline_template_1](https://user-images.githubusercontent.com/46112568/205901310-746c9a43-9ba2-46cb-baef-edd2ee9aadb9.png)

![inline_template_2](https://user-images.githubusercontent.com/46112568/205901335-b6fa988e-0a99-4a22-8565-24630b295462.png)

### Nesting Components

![nesting_components](https://user-images.githubusercontent.com/46112568/205901474-bfb1e342-8e86-4191-a7e8-e6b77e2c3ae4.png)

![nesting_components_result](https://user-images.githubusercontent.com/46112568/205901534-491ed3b8-96a2-4fc3-ac9a-6e2a448b063e.png)

