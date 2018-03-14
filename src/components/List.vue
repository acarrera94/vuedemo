<template>
<div>
<b-field position="is-centered">
            <b-input v-model="data" @keyup.enter="addItem" placeholder="List item" type="search" icon="plus">
            </b-input>
            <p class="control">
                <button @click='addItem' class="button is-danger">Add</button>
            </p>
    </b-field>
    <myTable :myList='myList'>
    </myTable>
</div>
</template>

<script>
export default {
  data () {
    return {
      data: '',
      myList: []
    }
  },
  methods: {
    addItem () {
      this.myList.push(this.data)
      console.log(this.myList.length)
    }
  }
}
</script>
