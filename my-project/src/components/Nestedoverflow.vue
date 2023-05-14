<template>
  <div class="parent" :style="{ height: parentHeight + 'px' }">
    <h1>aaaaaa</h1>
    <h1>bbbbbbb</h1>
    <h1>aaaaaa</h1>
    <h1>bbbbbbb</h1>
    <h1>aaaaaa</h1>
    <h1>bbbbbbb</h1>
    <div class="child" :style="{ height: childHeight + 'px' }">
      <h1>aaaaaa</h1>
      <h1>bbbbbbb</h1>
      <h1>aaaaaa</h1>
      <h1>bbbbbbb</h1>
      <h1>aaaaaa</h1>
      <h1>bbbbbbb</h1>
      <div class="nested" :style="{ height: nestedHeight + 'px' }">
        <h1>aaaaaa</h1>
        <h1>bbbbbbb</h1>
        <h1>aaaaaa</h1>
        <h1>bbbbbbb</h1>
        <h1>aaaaaa</h1>
        <h1>bbbbbbb</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NestedOverflowContainer",
  data() {
    return {
      parentHeight: 250,
      childHeight: 200,
      nestedHeight: 150,
    };
  },
};
</script>

<style>
.parent {
  border: 1px solid #ccc;
  overflow: auto;
}

.parent::-webkit-scrollbar {
  width: 16px;
}

.parent::-webkit-scrollbar-track {
  border-radius: 8px;
  background-color: #e7e7e7;
  border: 1px solid #cacaca;
}

.parent::-webkit-scrollbar-thumb {
  border-radius: 8px;
  border: 3px solid transparent;
  background-clip: content-box;
  background-color: #d55959;
}

.child {
  border: 1px solid blue;
  overflow: auto;
}

.nested {
  border: 1px solid green;
  overflow: auto;
}
</style>
