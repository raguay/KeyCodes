<script>
  let meta = false;
  let alt = false;
  let shift = false;
  let ctrl = false;
  let key = "";
</script>

<div
  id="main"
  tabindex="0"
  on:keydown|preventDefault={(e) => {
    meta = e.metaKey;
    alt = e.altKey;
    shift = e.shiftKey;
    ctrl = e.ctrlKey;
    key = e.key;
  }}
  on:keyup|preventDefault={(e) => {
    meta = e.metaKey;
    alt = e.altKey;
    shift = e.shiftKey;
    ctrl = e.ctrlKey;
    key = e.key;
  }}
>
  <h3>Checking keycodes</h3>
  <div class="row">
    <label for="metalabel">Meta Key</label>
    <p id="metalabel">{meta}</p>
  </div>
  <div class="row">
    <label for="shiftlabel">Shift Key</label>
    <p id="shiftlabel">{shift}</p>
  </div>
  <div class="row">
    <label for="altlabel">Alt Key</label>
    <p id="altlabel">{alt}</p>
  </div>
  <div class="row">
    <label for="ctrllabel">Ctrl Key</label>
    <p id="ctrllabel">{ctrl}</p>
  </div>
  <div class="row">
    <label for="keylabel">Key</label>
    <p id="keylabel">{key}</p>
  </div>
</div>

<style>
  #main {
    display: flex;
    flex-direction: column;
  }

  .row {
    display: flex;
    flex-direction: row;
  }

  label {
    margin: auto 20px;
  }
</style>
