# surplus on wheels: whatsapp bridge

WhatsAoo bridge for
[surplus on wheels (s+ow)](https://github.com/markjoshwel/surplus#on-termux-surplus-on-wheels).

s+ow bridges are defined in a file named `$HOME/.s+ow-bridges`. each command in the file is
ran, and comma-seperated target chat IDs are passed using stdin.

this bridge recognises targets prefixed with `wa:`.

```text
wa:<chat id>,...
```

to use the telegram bridge:

1. install [surplus](https://github.com/markjoshwel/surplus), mdtest and surplus on wheels

2. install git if not installed:

   ```text
   pkg install git
   ```

3. install spow-whatsapp-bridge:

   TODO

4. log into whatsapp:

   ```text
   s+ow-whatsapp-bridge
   ```

   give it a minute or two to sync your history. once the screen stops scrolling, you can
   safely exit.

5. add the following to your `$HOME/.s+ow-bridges` file:

   ```text
   s+ow-whatsapp-bridge
   ```

usage:

- `s+ow-whatsapp-bridge`  
  normal usage; sends latest message to `wa:`-prefixed targets given in stdin
- `s+ow-whatsapp-bridge logout`  
  logs out of WhatsApp
- `s+ow-whatsapp-bridge list`  
  lists all **group** chats and their IDs  
  for sending to individuals: their IDs are their internationalised phone numbers ending
  in `@s.whatsapp.net`.

  example: `+65 9000 0000` is `659000000@s.whatsapp.net`

## licence

the s+ow WhatsApp bridge is modified mdtest code, which is licensed under the Mozilla
Public License 2.0.
for more information, see [LICENCE](/LICENCE) or <https://www.mozilla.org/en-US/MPL/2.0/>.
