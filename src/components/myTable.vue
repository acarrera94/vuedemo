<template>
    <b-table
        :data="myList">
        <template slot-scope="props">
            <b-table-column centered='true'>
                {{ props.row }}
            </b-table-column>
        </template>
    </b-table>
</template>

<script>
export default {
  props: ['myList']
}
</script>
