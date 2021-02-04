# crypto
A secure and powerful encryption system made with php OOP with the help of openSSL.
To use simply include crypto.php in your project and create an instance of the class crypto with your encryption-decryption key(random digits or more and combination of letters and numbers) example:
<?php
$crypt = new crypto('37rhdgsjf94829344');
?>
To encrypt, call the method encrypt_text(plaintext) example:
<?php
echo $crypt->encrypt_text("I am batman");
?>
To decrypt, call the method decrypt_hash(encrypted-text) example:
<?php
echo $crypt->decrypt_hash('NsbVnidhojL+jxr+M4Odogm4hGwcUAXIsnHQI85ij7+80XezvVRc7fLnu8KdNFGRWZqKbLBcpjkNeYsXpOu9+g==');
?>

This library can also be used to encrypt and decrypt url GET requests along with normal texts
For urls, wrap the encrypt_text() method inside urlencode example:
<a href"text.php?text=<?php echo urlencode($crypt->encrypt_text("Iam batman")); ?>"></a>
And decrypt normally as already stated above.
Security comes first

