# Divi-RTL
Fixing column structure when RTL Langauge it is used.

## How to use it

### 1. Directly into Divi
You can copy the CSS  code from `dt-rtl.css` file directly into Divi ➤ Theme Options ➤ Custom CSS

### 2. Unsing a child theme
If you already have a child theme installed, then in your child theme folder create a new folder called **css**

In the **css** folder create a new CSS file called `dt-rtl.css` and put the code from this Git

In `functions.php` of your child theme add this PHP code:
```
function dt_load_rtl_styles(){
    wp_enqueue_style( 'dt-rtl-columns-fix', get_stylesheet_directory_uri() . '/css/dt-rtl.css' );
}

if (is_rtl()){
    add_action( 'get_footer', 'dt_load_rtl_styles' );
}
```

*Note: If you want you can use the minified version, just don't forget to update the PHP code in order to load the minified version*