# Lesson-17-regular-expressions (RegEx)

## Rules
<div align="center">
    <table >
<tr class=""><th class="" style="height: 47.2px;"><span class=""><div >[abc]</div></span></th><td class="" style="height: 47.2px;"><span class=""><div >A certain character, in this case a, b or c.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >[^abc]</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any character except a, b or c.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >[a-z]</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any character from a to z. Lowercase letters only.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >[^a-z]</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any character except lowercase and a to z.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >[a-zA-Z]</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any small and large character from a, or rather A to z, or rather Z.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >.</div></span></th><td class=" " style="height: 47.2px;"><span class="">Any character.</span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >\s</div></span></th><td class=" " style="height: 47.2px;"><span class="">Any <span class="" style="color: rgba(0, 0, 0, 0.87);">whitespace character</span></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >\S</div></span></th><td class=" " style="height: 47.2px;"><span class="">Any non-<span class="" style="color: rgba(0, 0, 0, 0.87);">whitespace character</span></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >\d</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any number.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >\D</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any character except a number.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >\w</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any letter.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >\W</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any character except a letter.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >(...)</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >The parentheses wrap a certain set.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >(a|b)</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Character a or character b.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >a?</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >A maximum of one character a (one or none).</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >a*</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Any number of characters a (or neither).</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >a+</div></span></th><td class=" " style="height: 47.2px;"><span class="">At least one character a (one or more).</span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >a{3}</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >3 characters a.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >a{3,}</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >3 or more characters a.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >a{3,6}</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >3 to 6 characters a.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >^</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >Start of text.</div></span></td></tr><tr class=""><th class=" " style="height: 47.2px;"><span class=""><div >$</div></span></th><td class=" " style="height: 47.2px;"><span class=""><div >End of text.</div></span></td></tr>
    </table>
    </div>
    
## Related sources

- [regex101.com](https://regex101.com/)
- [Regex Cheatsheet](https://cheatography.com/davechild/cheat-sheets/regular-expressions/pdf)
- [Regular Expression Library](https://regexlib.com/Search.aspx?k=ZIP+codes&c=-1&m=-1&ps=20)


## Excercise
<div class="uu5-common-div uucontentkit-bricks-content"><div class="uu5-common-div uu5-richtext-block uu-richtext-eiserq" id="4d4cb15a288054317b86c005af62c000-inner"><ol class="uu5-bricks-ol"><li class=" uu5-bricks-li"><span class="uu-bricks-j5rkb3">Write a regular expression to validate iso date and time (e.g.: 2019-12-04T07:07:35+01:00)</span></li>

Basic:

    `\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}[+-]\d{2}:\d{2}`

Intermediate 😄: 

    `(?<year>\d{4})-(?<month>0[1-9]|1[1-2])-(?<day>[012][0-9]|3[01])T(?<hour>[012][0-9]):(?<minutes>[05][0-9]):(?<second>[0-5][0-9])(?<offset>[+-](0[0-9]|1[1-2]):([05][0-9]))`
                                                                                                                                                                                                                                                                                                                                                               
<li class=" uu5-bricks-li"><span class="uu-bricks-j5rkb3">Use a regular expression to get the day, month, and year from the previous iso notation.</span></li>


<li class=" uu5-bricks-li"><span class="uu-bricks-j5rkb3">Write a regular expression to validate the generic id, which can only contain numbers and letters a-f, has a maximum of 8 characters and can also contain a question mark at the beginning (eg ?a582fd10 or 0ba99cc1). Write the regular expression to a function that will validate its input and return a boolean.</span></li>

    `\??[a-zA-Z0-9]{8}`


<li class=" uu5-bricks-li"><span class="uu-bricks-j5rkb3">Write a regular expression for zip code validation. It must contain exactly five digits, and the third digit may (but need not) be followed by a space.<br>Example of a valid zip code: <code id="dbb384a98d1994435aba6cf77bd382d2-code" class="uu5-bricks-_code uu5-bricks-code">120 00</code> and <code id="6b1939252bb2c44fd9fdbefd7a8e3393-code" class="uu5-bricks-_code uu5-bricks-code">12000</code>.</span></li>

        `\d{5}|\d{3} \d{2}`

<li class=" uu5-bricks-li"><span class="uu-bricks-j5rkb3">Write a regular expression for phone number validation. It must contain ninie digits plus country code, and can be separated by spaces betweeen each three digits of prone number and also between country code and phone number.</li> <code id="dbb384a98d1994435aba6cf77bd382d2-code" class="uu5-bricks-_code uu5-bricks-code">420 123 456 789
</code> but also <code id="6b1939252bb2c44fd9fdbefd7a8e3393-code" class="uu5-bricks-_code uu5-bricks-code">+420 123 456 789</code>, <code id="6b1939252bb2c44fd9fdbefd7a8e3393-code" class="uu5-bricks-_code uu5-bricks-code">+420 123456789</code> or even  <code id="6b1939252bb2c44fd9fdbefd7a8e3393-code" class="uu5-bricks-_code uu5-bricks-code">+77 123456789</code> for some another country.

</ol></div></div> 

    Result:
        
     `\+?\d{1,3}\s?\d{3}\s?\d{3}\s?\d{3}`




