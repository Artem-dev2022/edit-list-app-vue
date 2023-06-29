<script>
export default {
    data() {
        return {
            form: {
                current: this.array[0],
            },
            inputValue: this.array[0].value,
        }
    },
    props: ['array'],
    methods: {
        handleClick(e) {
            this.form.current = this.array[e]
            this.inputValue = this.array[e].value
        },
        onSubmit() {
            this.form.current.value = this.inputValue
        }
    }
}
</script>

<template>
    <h1>Элементы массива:</h1>
    <div class="wrapper">
        <el-table :data="array" border style="width: fit-content">
            <el-table-column prop="name" label="Name" width="180" />
            <el-table-column prop="value" label="Value" width="180" />
            <el-table-column fixed="right" label="Operations" width="120">
                <template #default="scope">
                    <el-button type="primary" size="small" @click.prevent="handleClick(scope.$index)">Edit Value</el-button>
                </template>
            </el-table-column>
        </el-table>

        <el-form label-width="120px" class="form">
            <h2>{{ form.current.name }}</h2>
            <label>
                Value:
                <el-input v-model="inputValue" />
            </label>
            <el-button class="form__btn" type="primary" @click="onSubmit">Save</el-button>
        </el-form>
    </div>
</template>

<style scoped>
h1 {
    font-size: 24px;
}
.wrapper {
    position: relative;
    display: flex;
    gap: 50px;
    margin-bottom: 50px;
}
.form {
    position: sticky;
    top: 0;
    padding: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: fit-content;
}
label {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-bottom: 20px;
}
h2 {
    margin: 0 0 18px 0;
    text-align: center;
}
</style>
