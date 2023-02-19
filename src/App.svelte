<script>
  import mainLogo from "./assets/demo2.png";
  import Counter from "./lib/Counter.svelte";
  import Counters from "./lib/Counters.svelte";
</script>

<main>
  <div class="wrap">
    <header>
      <div class="header-left">
        <div class="header-menu" />
        <a class="header-logo" href="/">
          <!-- <img src={mainLogo} alt="로고" />
           <img src="/src/assets/demo2.png" alt="로고" /> -->
        </a>
      </div>
      <div class="header-toolbar">
        <div class="header-toolbtn">
          <img src="/src/assets/ico_search.svg" alt="검색" />
        </div>
        <div class="header-toolbtn">
          <span class="bullet animation-blink" />
          <img src="/src/assets/ico_search.svg" alt="검색" />
        </div>
        <div class="header-toolbtn">
          <img src="/src/assets/ico_search.svg" alt="검색" />
        </div>
      </div>
    </header>
    <div class="title">
      <div class="title-left">
        <h1>DASHBOARD</h1>
        <ul class="breadcrum">
          <li><a href="#">home</a></li>
          <li>-</li>
          <li><a href="#">dashboards</a></li>
          <li>-</li>
          <li><a href="#">default</a></li>
        </ul>
      </div>
      <div class="title-right">
        <a href="/" class="btn btn-white"> filter </a>
      </div>
    </div>

    <div class="card">
      <Counter />
      <Counters />
    </div>
  </div>
</main>

<style>
  .wrap {
    width: 100vw;
    background: url(/src/assets/header-bg.jpg);
    background-size: 100% 200px;
    background-repeat: no-repeat;
  }

  /* header */
  header {
    display: flex;
    /* justify-content: space-between; */
    align-items: center;
    height: 65px;
    border-bottom: var(--bs-header-tablet-and-mobile-default-border);
    padding: 0 15px;
  }
  .header-left {
    flex-grow: 1;
  }
  .header-logo {
    display: block;
    height: 30px;
    width: 35px;
    background: url(/src/assets/demo2.png) 50% 50% no-repeat;
    background-size: contain;
  }
  .header-toolbtn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0;
    width: 30px;
    height: 30px;
    border-radius: 5px;
  }
  .header-toolbtn {
    position: relative;
  }
  .header-toolbtn span.bullet {
    background-color: green;
    width: 6px;
    height: 6px;
    border-radius: 100% !important;
    position: absolute;
    top: 0px;
    left: 50%;
    transform: translate(-50%, -50%) !important;
  }
  .header-toolbtn:hover {
    background-color: rgba(255, 255, 255, 0.1);
    cursor: pointer;
  }
  /* //header */
  .title {
    padding: 0 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #fff;
  }
  .title h1 {
    font-size: 1rem;
    font-weight: 600;
    text-align: left;
    margin: 4px 0;
  }
  .title-left .breadcrum {
    font-size: 0.75rem;
    opacity: 0.75;
    display: flex;
    gap: 0 4px;
    margin: 4px 0;
  }
  .title-left .breadcrum a {
    color: #fff;
  }
  .title-left .breadcrum a:hover {
    color: blue;
  }

  .title-left {
    display: flex;
    flex-direction: column;
  }

  .title-right .btn {
    color: var(--bs-white-inverse);
    border-color: var(--bs-white);
    background-color: var(--bs-white) !important;
    border: 0;
    padding: calc(0.775rem + 1px) calc(1.5rem + 1px);
    color: var(--bs-text-white);
    display: inline-flex;
    align-items: center;
  }

  .animation-blink {
    animation: animationBlink 1s steps(5, start) infinite;
  }

  @keyframes animationBlink {
    to {
      visibility: hidden;
    }
  }
</style>
