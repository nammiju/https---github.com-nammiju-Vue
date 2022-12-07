<template>
  <form>
        <h3 v-if="check">회원조회/수정</h3>
        <h3 v-else>회원가입</h3>
        ID: <input type="text" v-model="id" id="id" :readonly="check"><br>
        PW: <input type="text" v-model="password" id="password"><br>
        이름: <input type="text" v-model="name" id="name"><br>
        권한: <select v-model="role">
                <option value="default" disabled>::선택::</option>
                <option value="User">일반유저</option>
                <option value="Admin">관리자</option>
            </select><br>
        <button type="button" @click="userUpdate" v-if="check">수정</button>
        <button type="button" @click="userInsert" v-else>등록</button>
        <button type="button" @click="reset">취소</button>
  </form>
</template>

<script>
export default {
  name: 'UserForm'
}
</script>

<style>

</style>