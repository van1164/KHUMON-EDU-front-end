<script>
    import MainPage from "./MainPage.svelte";

    let id = sessionStorage.getItem("id")
    let accessCode = sessionStorage.getItem("access-code")
    let nickName = sessionStorage.getItem("nickname")


</script>

{#if accessCode}
<MainPage/>

{:else}
<div class="grid place-items-center" >
<img src="images/khu_mon_logo.png" alt="logo" width="50%" style=" margin-bottom: 5%;" >
</div>


<div style=" display:flex; justify-content: space-between; margin-top: 5%; margin-bottom: 5%">
<div style="width: 40%; height: 1px; background-color: lightgrey; margin: auto"></div>
<div style="font-weight: bold; color:black; font-size:xx-large">Login</div>
<div style="width: 40%; height: 1px; background-color: lightgrey; margin: auto"></div>
</div>

<div style="margin:auto; width: 40%; height: 100%; display:col; justify-content: space-between; flex-direction:column">
    <div class=" justify-center">
        <a href="https://khumon-edu.kro.kr/oauth2/authorization/google"><img src="images/google_login.png" alt="logo" width="100%" class=" justify-center"></a>
    </div>

    <div>
        <a href="https://khumon-edu.kro.kr/oauth2/authorization/kakao"><img src="images/kakao_login.png" alt="logo"  width="100%"></a>
    </div>

    <div>
        <a href="https://khumon-edu.kro.kr/oauth2/authorization/naver"><img src="images/naver_login.png" alt="logo"  width="100%"></a>
    </div>

</div>

{/if}