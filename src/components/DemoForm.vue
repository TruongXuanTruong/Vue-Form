<template>
    <section class="container">
        <h1>Demo Form</h1>
        <form @submit.prevent="handleSubmit">
            <!-- <div class="form-group">
                <label for="taikhoan">Tai Khoan</label>
                <input type="text" 
                class="form-control" 
                id="taiKhoan" 
                v-model="taiKhoan"
                />
            </div> -->
            <div class="form-group">
                <label for="baiLam">Bài Làm</label>
                <textarea 
                    class ="form-control"
                    id="baiLam"
                    rows="20"
                    v-model="vanMau"
                >   
                </textarea>  
            </div>
            <br/>
            <div class="form-check">
                
                <input type="checkbox" 
                class="form-check-input" 
                id="isSave" 
                v-model="isSave"
                />
                <label class="form-check-label" for="isSave">Bạn có muốn lưu Tài Khoản không ?</label>
            </div>
            <br/>
            <div>
                <h1>Bạn đang sống ở đâu ?</h1>
                <div class="form-check">
                    <input type="checkbox" class="form-check-input" value="Thủ Đô Hà Nội" v-model="noiSinhSong" />
                    <label class="form-check-label">Thủ Đô Hà Nội</label>
                </div>
                <div class="form-check">
                    <input type="checkbox" class="form-check-input" value="Thành Phố Hồ Chí Minh" v-model="noiSinhSong" />
                    <label class="form-check-label">Thành Phố Hồ Chí Minh</label>
                </div>
                <div class="form-check">
                    <input type="checkbox" class="form-check-input" value="Hưng Yên" v-model="noiSinhSong" />
                    <label class="form-check-label">Hưng Yên</label>
                </div>
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
            taiKhoan: "",
            vanMau: "Đề bài : Viết cảm nhận của bạn ",
            isSave: false,
            noiSinhSong: [],
        };
    },
    methods : {
        handleSubmit(){
            console.log(this.taiKhoan);
            console.log(this.vanMau);
            console.log(this.isSave);
            console.log(this.noiSinhSong);
        },
    }
})
</script>

<style>
.form-check {
    display: flex;
    justify-content: center;
    align-items: center;
}

.form-check-input {
    margin-right: 8px; 
}
</style>
