# ceaserChiper

function caesarCipher(str, shift) {

    const alphabetArr = "abcdefghijklmnopqrstuvwxyz".split("");
    let res = "";



    for (let i = 0; i < str.length; i++) {
        const char = str[i];
        const idx = alphabetArr.indexOf(char);


        if (idx === -1) {
            res += char;
            continue;
        }
        const encodedIdx = (idx + shift) % 26;

        res += alphabetArr[encodedIdx];


    }
    return res;
}
