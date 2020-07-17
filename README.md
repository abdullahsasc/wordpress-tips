## WordPress Tips by Noman 👀

#### How to Add an Admin User in WordPress using FTP 

You need to access your theme functions file. Then Ctrl+C and Ctrl+V and change the Username, Password, Email you rock 👀

>Pro tips: Use Child theme wp-content/themes/your-theme-child/functions.php 🐱‍🏍

``` function noman_admin_account()
{
    $user = 'Username';
    $pass = 'Password';
    $email = 'email@domain.com';
    if (!username_exists($user)  && !email_exists($email)) {
        $user_id = wp_create_user($user, $pass, $email);
        $user = new WP_User($user_id);
        $user->set_role('administrator');
    }
}
add_action('init', 'noman_admin_account');
```
