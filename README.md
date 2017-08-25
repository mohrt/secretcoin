# Secret Coin

Store your secrets securely.

## Description

Storing sensitive data can be problematic. If it gets accidentally lost or destroyed, you lose your data. If stolen, your data is compromised. You can make multiple copies and store them in isolation, but this increases the risk of being stolen or misplaced. You can encrypt them, but then you face the same problem storing the encryption key.

Secret Coin uses [Shamir's Secret Sharing](https://en.wikipedia.org/wiki/Shamir%27s_Secret_Sharing) algorithm to divide your secret into multiple (N) shares, and then you can restore the secret using a specified number of the shares (M of N). None of the shares contain identifiable information about the secret. If any share, or up to (M-1) shares are compromised, the secret is still completely unknown.

This type of security model is critical for data such as Bitcoin mnemonic phrases, private keys, or anything giving one "keys to the kingdom."

You will need to access the tool via an HTTP URL on a browser, and not direct file:// access. Example: http://localhost:8000. Detailed instructions follow.

### Prerequisites

You will need:

* The [.zip](https://github.com/mohrt/secretcoin) archive of this repository (get from GitHub Download button)
* python scripting language. This comes with OSX. PC users may need to install python, or use another web server implementation, out of scope for these docs.
* HTML5 compatible browser such as Google Chrome

### Installing

These commands are ran from the terminal.

unzip the archive
```
unzip secretcoin-master.zip
```

change to directory
```
cd secretcoin-master
```

start Simple HTTP Server
```
python -m SimpleHTTPServer 8000
```

Visit the website in your browser
```
http://localhost:8000
```

## Paste or type in a secret, such as mnemonic phrase or private key.

There is a text area for this.

## Chooose the total number of shares, and required number to restore the secret.

For example, you might want to split your secret into three separate shares, and require any two of three shares to restore the secret.

## Click Generate

This will generate the shares.

## Download the individual shares

This will create individual files, one for each share.

## TEST THE RESTORE

It is absolutely crucial that you test the restore. Choose the required number of shares and be sure the secret is regenerated correctly.

## Save the shares separately.

You may choose to place the shares on separate USB thumb drives, then store these drives in three separate, safe locations. You could also print the shares and store the paper copies.

## Built With

* [Samir's Secret Sharing](https://en.wikipedia.org/wiki/Shamir%27s_Secret_Sharing) - The algorithm
* [secret.js](https://github.com/amper5and/secrets.js/) - Javascript implementation of SSS
* [Vue.js](https://vuejs.org/) - Javascript tool
* [JQuery](https://jquery.com/) - Javascript tool
* [Skeleton](http://getskeleton.com/) - CSS/Javascript tool

## Contributing

Use the [GitHub](https://github.com/mohrt/secretcoin) repository to create a pull request.

## Authors

* **Monte Ohrt** - *Initial work* - [mohrt](https://github.com/mohrt)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
