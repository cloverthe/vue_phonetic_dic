<template>
  <form>
    <input type="text" v-model="input" />
  </form>
  <p>🇬🇧 {{ encodeInputEN }}</p>
  <p>🇩🇪 {{ encodeInputDE }}</p>
  <p>🇷🇺 {{ encodeInputRU }}</p>
  <p>{{ encodeInputNEW }}</p>

  <!-- <h1>{{ encodeInput() }}</h1> -->
</template>
<script>
export default {
  data() {
    return { input: "" };
  },
  computed: {
    encodeInputNEW() {
      let dic = ["Alef", "Buka"];
      let encoded = [];
      [...this.input.toLowerCase()].forEach((letter) => {
        let word = dic.filter((s) => s.startsWith(letter.toUpperCase()))[0];
        encoded.push(word);
      });
      return encoded.join(" ");
    },
    // a computed getter
    encodeInputEN() {
      let encoded = "";
      [...this.input.toLowerCase()].forEach((letter) => {
        switch (letter) {
          case "a":
            encoded += " Alfa";
            break;
          case "b":
            encoded += " Bravo";
            break;
          case "c":
            encoded += " Charlie";
            break;
          case "d":
            encoded += " Delta";
            break;
          case "e":
            encoded += " Echo";
            break;
          case "f":
            encoded += " Foxtrot";
            break;
          case "G":
            encoded += " Golf";
            break;
          case "H":
            encoded += " Hotel";
            break;
          case "i":
            encoded += " India";
            break;
          case "J":
            encoded += " Juliet";
            break;
          case "k":
            encoded += " Kilo";
            break;
          case "l":
            encoded += " Lima";
            break;
          case "m":
            encoded += " Mike";
            break;
          case "n":
            encoded += " November";
            break;
          case "o":
            encoded += " Oscar";
            break;
          case "p":
            encoded += " Papa";
            break;
          case "q":
            encoded += " Quebec";
            break;
          case "r":
            encoded += " Romeo";
            break;
          case "s":
            encoded += " Sierra";
            break;
          case "t":
            encoded += " Tango";
            break;
          case "u":
            encoded += " Uniform";
            break;
          case "v":
            encoded += " Victor";
            break;
          case "w":
            encoded += " Whiskey";
            break;
          case "x":
            encoded += " X-ray";
            break;
          case "y":
            encoded += " Yankee";
            break;
          case "z":
            encoded += " Zulu";
            break;
        }
      });
      return encoded;
    },
    encodeInputRU() {
      let encoded = "";
      [...this.input.toLowerCase()].forEach((letter) => {
        switch (letter) {
          case "а":
            encoded += " Антон";
            break;
          case "б":
            encoded += " Борис";
            break;
          case "в":
            encoded += " Василий";
            break;
          case "г":
            encoded += " Григорий";
            break;
          case "д":
            encoded += " Дмитрий";
            break;
          case "е":
            encoded += " Елена";
            break;
          case "ё":
            encoded += " Ёлка";
            break;
          case "ж":
            encoded += " Женя";
            break;
          case "з":
            encoded += " Зинаида";
            break;
          case "и":
            encoded += " Иван";
            break;
          case "й":
            encoded += " Иван краткий";
            break;
          case "к":
            encoded += " Константин";
            break;
          case "л":
            encoded += " Леонид";
            break;
          case "м":
            encoded += " Михаил";
            break;
          case "н":
            encoded += " Николай";
            break;
          case "о":
            encoded += " Ольга";
            break;
          case "п":
            encoded += " Павел";
            break;
          case "р":
            encoded += " Роман";
            break;
          case "с":
            encoded += " Семён";
            break;
          case "т":
            encoded += " Татьяна";
            break;
          case "у":
            encoded += " Ульяна";
            break;
          case "ф":
            encoded += " Фёдор";
            break;
          case "х":
            encoded += " Харитон";
            break;
          case "ц":
            encoded += " Цапля";
            break;
          case "ч":
            encoded += " Человек";
            break;
          case "ш":
            encoded += " Шура";
            break;
          case "щ":
            encoded += " Щука";
            break;
          case "ъ":
            encoded += " Твёрдый знак";
            break;
          case "ы":
            encoded += " Еры";
            break;
          case "ь":
            encoded += " Мягкий знак";
            break;
          case "э":
            encoded += " Эхо";
            break;
          case "ю":
            encoded += " Юрий";
            break;
          case "я":
            encoded += " Яков";
            break;
        }
      });
      return encoded;
    },
    encodeInputDE() {
      let encoded = "";

      [...this.input.toLowerCase()].forEach((letter, index) => {
        switch (letter) {
          case "a":
            encoded += " Anton";
            break;
          case "b":
            encoded += " Berta";
            break;
          case "c":
            if (
              this.input[index - 1] !== "s" &&
              this.input[index + 1] !== "h"
            ) {
              encoded += " Cäsar";
            }
            break;
          case "d":
            encoded += " Dora";
            break;
          case "e":
            encoded += " Emil";
            break;
          case "f":
            encoded += " Friedrich";
            break;
          case "g":
            encoded += " Gustav";
            break;
          case "h":
            if (
              this.input[index - 1] !== "c" &&
              this.input[index + 2] !== "s"
            ) {
              encoded += " Heinrich";
            }

            break;
          case "i":
            encoded += " Ida";
            break;
          case "j":
            encoded += " Julius";
            break;
          case "k":
            encoded += " Kaufman";
            break;
          case "l":
            encoded += " Ludwig";
            break;
          case "m":
            encoded += " Martha";
            break;
          case "n":
            encoded += " Nordpol";
            break;
          case "o":
            encoded += " Otto";
            break;
          case "ö":
            encoded += " Ökonom";
            break;
          case "p":
            encoded += " Paula";
            break;
          case "q":
            encoded += " Quelle";
            break;
          case "r":
            encoded += " Richard";
            break;
          case "ä":
            encoded += " Äpfel";
            break;
          case "s":
            if (
              this.input[index + 1] === "c" &&
              this.input[index + 2] === "h"
            ) {
              encoded += " Schule";
            } else {
              encoded += " Samuel";
            }

            break;
          case "t":
            encoded += " Theodor";
            break;
          case "u":
            encoded += " Ulrich";
            break;
          case "ü":
            encoded += " Übermut";
            break;
          case "v":
            encoded += " Viktor";
            break;
          case "w":
            encoded += " Wilhelm";
            break;
          case "x":
            encoded += " Xanthippe";
            break;
          case "y":
            encoded += "Ypsilon";
            break;
          case "z":
            encoded += " Zacharias";
            break;
        }
      });
      return encoded;
    },
  },
};
</script>
<style scoped></style>
