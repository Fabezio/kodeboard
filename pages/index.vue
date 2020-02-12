<template lang="pug">
div
  .keyboard


    .touch
      .letter ²

      .char
        span 1
        span &

      .char
        span 2
        span é
      .char
        span 3
        span "
      .char
        span 4
        span '
      .char
        span 5
        span (
      .char
        span 6
        span -
      .char
        span 7
        span è
      .char
        span 8
        span _
      .char
        span 9
        span ç
      .char
        span 0
        span à
      .char
        span °
        span )
      .char
        span +
        span =
      .backsp
        span backsp

    .touch
      .tab.center-items tab
      .letter(v-for='(char, i) in row1' :key='i')
        span {{char}}

      .char
        span ¨
        span ^

      .char
        span £
        span $

    .touch
      .caps CAPS
      .letter(v-for='(char) in row2')
        span {{char}}
      .char
        span %
        span ù
      .char
        span ù
        span `


    .touch
      .tab maj
      .char
        span >
        span <
      .letter(v-for='(char) in row3')
        span {{char}}
      .char
        span ?
        span ,
      .char
        span .
        span ;
      .char
        span /
        span :
      .char
        span +
        | =

</template>

<script>
export default {
  data() {
    return {
      row1: Array.from('AZERTYUIOP'),
      row2: Array.from('qsdfghjklm'),
      row3: Array.from('wxcvbn')
    }
  }
}
</script>

<style>
.keyboard {
  margin: auto;
}
.touch {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}
.char,
.letter,
.tab,
.caps,
.shift,
.backsp {
  display: table-cell;
  height: 50px;
  background-color: #4287f5;
  margin: 2px;
  padding: auto 0;
  color: whitesmoke;
  vertical-align: middle;
  text-align: center;
  border: state black 2px;
  border-radius: 3px;
}
.tab {
  width: 70px;
}
.caps {
  width: 80px;
}
.shift {
  width: 60px;
}
.letter {
  width: 50px;
  text-transform: uppercase;
}
.backsp {
  width: 100px;
}
.char {
  width: 50px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
