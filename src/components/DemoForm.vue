<template>
    <section class="container">
        <h1>Demo Form</h1>
        <form @submit.prevent="handleSubmit">
            <div class="form-group">
                <label for="taikhoan">Tai Khoan</label>
                <input type="text" 
                class="form-control" 
                id="taiKhoan" 
                v-model="taiKhoan"
                />
            </div>
            <button type="submit" class="btn btn-success">
                Submit
            </button>
        </form>
    </section>
</template>

<script>
export default ({
    data() {
        return {
            taiKhoan: ""
        };
    },
    methods : {
        handleSubmit(){
            console.log(this.taiKhoan);
        },
    }
})
</script>

<style>

</style>
