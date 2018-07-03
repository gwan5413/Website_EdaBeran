---
ID: 748
post_title: Sigup
author: asenclothing
post_excerpt: ""
layout: page
permalink: https://edaberan.com/sigup/
published: true
post_date: 2018-07-03 16:21:07
---
<pre><span id="line-1"><span class="cp">&lt;?php</span> <span class="k">if</span> <span class="p">(</span> <span class="nx">get_option</span><span class="p">(</span> <span class="s1">'woocommerce_enable_myaccount_registration'</span> <span class="p">)</span> <span class="o">===</span> <span class="s1">'yes'</span> <span class="p">)</span> <span class="o">:</span> <span class="cp">?&gt;</span>
</span><span id="line-2">
</span><span id="line-3"><span class="x">    &lt;div class="row"&gt;</span>
</span><span id="line-4"><span class="x">      &lt;div class="col-xs-12 col-sm-8 col-sm-offset-2"&gt;</span>
</span><span id="line-5"><span class="x">        &lt;div class="row"&gt;</span>
</span><span id="line-6">
</span><span id="line-7">        <span class="cp">&lt;?php</span> <span class="k">if</span><span class="p">(</span> <span class="nb">isset</span><span class="p">(</span> <span class="nv">$_GET</span><span class="p">[</span><span class="s1">'action'</span><span class="p">])</span> <span class="o">&amp;&amp;</span> <span class="nv">$_GET</span><span class="p">[</span><span class="s1">'action'</span><span class="p">]</span> <span class="o">==</span> <span class="s2">"register"</span><span class="p">)</span> <span class="o">:</span> <span class="cp">?&gt;</span>
</span><span id="line-8">
</span><span id="line-9"><span class="x">            &lt;div class="col-xs-12"&gt;</span>
</span><span id="line-10">
</span><span id="line-11"><span class="x">                &lt;form method="post" class="box"&gt;</span>
</span><span id="line-12">
</span><span id="line-13"><span class="x">                  &lt;h5 class="headline"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Sign Up'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">&lt;/h5&gt;</span>
</span><span id="line-14">
</span><span id="line-15">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'woocommerce_register_form_start'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-16">
</span><span id="line-17">                    <span class="cp">&lt;?php</span> <span class="k">if</span> <span class="p">(</span> <span class="s1">'no'</span> <span class="o">===</span> <span class="nx">get_option</span><span class="p">(</span> <span class="s1">'woocommerce_registration_generate_username'</span> <span class="p">)</span> <span class="p">)</span> <span class="o">:</span> <span class="cp">?&gt;</span>
</span><span id="line-18">
</span><span id="line-19"><span class="x">                        &lt;p class="form-row form-row-wide"&gt;</span>
</span><span id="line-20"><span class="x">                            &lt;label for="reg_username"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Username'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x"> &lt;span class="required"&gt;*&lt;/span&gt;&lt;/label&gt;</span>
</span><span id="line-21"><span class="x">                            &lt;input type="text" class="input-text" name="username" id="reg_username" value="</span><span class="cp">&lt;?php</span> <span class="k">if</span> <span class="p">(</span> <span class="o">!</span> <span class="k">empty</span><span class="p">(</span> <span class="nv">$_POST</span><span class="p">[</span><span class="s1">'username'</span><span class="p">]</span> <span class="p">)</span> <span class="p">)</span> <span class="k">echo</span> <span class="nx">esc_attr</span><span class="p">(</span> <span class="nv">$_POST</span><span class="p">[</span><span class="s1">'username'</span><span class="p">]</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">" /&gt;</span>
</span><span id="line-22"><span class="x">                        &lt;/p&gt;</span>
</span><span id="line-23">
</span><span id="line-24">                    <span class="cp">&lt;?php</span> <span class="k">endif</span><span class="p">;</span> <span class="cp">?&gt;</span>
</span><span id="line-25">
</span><span id="line-26"><span class="x">                    &lt;p class="form-row form-row-wide"&gt;</span>
</span><span id="line-27"><span class="x">                        &lt;label for="reg_email"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Email address'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x"> &lt;span class="required"&gt;*&lt;/span&gt;&lt;/label&gt;</span>
</span><span id="line-28"><span class="x">                        &lt;input type="email" class="input-text" name="email" id="reg_email" value="</span><span class="cp">&lt;?php</span> <span class="k">if</span> <span class="p">(</span> <span class="o">!</span> <span class="k">empty</span><span class="p">(</span> <span class="nv">$_POST</span><span class="p">[</span><span class="s1">'email'</span><span class="p">]</span> <span class="p">)</span> <span class="p">)</span> <span class="k">echo</span> <span class="nx">esc_attr</span><span class="p">(</span> <span class="nv">$_POST</span><span class="p">[</span><span class="s1">'email'</span><span class="p">]</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">" /&gt;</span>
</span><span id="line-29"><span class="x">                    &lt;/p&gt;</span>
</span><span id="line-30">
</span><span id="line-31">                    <span class="cp">&lt;?php</span> <span class="k">if</span> <span class="p">(</span> <span class="s1">'no'</span> <span class="o">===</span> <span class="nx">get_option</span><span class="p">(</span> <span class="s1">'woocommerce_registration_generate_password'</span> <span class="p">)</span> <span class="p">)</span> <span class="o">:</span> <span class="cp">?&gt;</span>
</span><span id="line-32">
</span><span id="line-33"><span class="x">                        &lt;p class="form-row form-row-wide"&gt;</span>
</span><span id="line-34"><span class="x">                            &lt;label for="reg_password"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Password'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x"> &lt;span class="required"&gt;*&lt;/span&gt;&lt;/label&gt;</span>
</span><span id="line-35"><span class="x">                            &lt;input type="password" class="input-text" name="password" id="reg_password" /&gt;</span>
</span><span id="line-36"><span class="x">                        &lt;/p&gt;</span>
</span><span id="line-37">
</span><span id="line-38">                    <span class="cp">&lt;?php</span> <span class="k">endif</span><span class="p">;</span> <span class="cp">?&gt;</span>
</span><span id="line-39">
</span><span id="line-40"><span class="x">                    &lt;!-- Spam Trap --&gt;</span>
</span><span id="line-41"><span class="x">                    &lt;div style="</span><span class="cp">&lt;?php</span> <span class="k">echo</span> <span class="p">(</span> <span class="p">(</span> <span class="nx">is_rtl</span><span class="p">()</span> <span class="p">)</span> <span class="o">?</span> <span class="s1">'right'</span> <span class="o">:</span> <span class="s1">'left'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">: -999em; position: absolute;"&gt;&lt;label for="trap"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Anti-spam'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">&lt;/label&gt;&lt;input type="text" name="email_2" id="trap" tabindex="-1" /&gt;&lt;/div&gt;</span>
</span><span id="line-42">
</span><span id="line-43">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'woocommerce_register_form'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-44">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'register_form'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-45">
</span><span id="line-46"><span class="x">                    &lt;p class="form-row"&gt;</span>
</span><span id="line-47">                        <span class="cp">&lt;?php</span> <span class="nx">wp_nonce_field</span><span class="p">(</span> <span class="s1">'woocommerce-register'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-48"><span class="x">                        &lt;input type="submit" class="button" name="register" value="</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Register'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">" /&gt;</span>
</span><span id="line-49"><span class="x">                    &lt;/p&gt;</span>
</span><span id="line-50">
</span><span id="line-51">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'woocommerce_register_form_end'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-52">
</span><span id="line-53"><span class="x">                &lt;/form&gt;</span>
</span><span id="line-54">
</span><span id="line-55"><span class="x">            &lt;/div&gt; &lt;!-- end Register Section .col-sm-6 --&gt;</span>
</span><span id="line-56">
</span><span id="line-57">        <span class="cp">&lt;?php</span> <span class="k">else</span> <span class="o">:</span> <span class="cp">?&gt;</span>
</span><span id="line-58">
</span><span id="line-59"><span class="x">          &lt;div class="col-xs-12"&gt;</span>
</span><span id="line-60">
</span><span id="line-61"><span class="x">                &lt;form method="post" class="box"&gt;</span>
</span><span id="line-62">
</span><span id="line-63"><span class="x">                  &lt;h5 class="headline"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Login'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">&lt;/h5&gt;</span>
</span><span id="line-64">
</span><span id="line-65">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'woocommerce_login_form_start'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-66">
</span><span id="line-67"><span class="x">                    &lt;p class="form-row form-row-wide"&gt;</span>
</span><span id="line-68"><span class="x">                        &lt;label for="username"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Username or email address'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x"> &lt;span class="required"&gt;*&lt;/span&gt;&lt;/label&gt;</span>
</span><span id="line-69"><span class="x">                        &lt;input type="text" class="input-text" name="username" id="username" value="</span><span class="cp">&lt;?php</span> <span class="k">if</span> <span class="p">(</span> <span class="o">!</span> <span class="k">empty</span><span class="p">(</span> <span class="nv">$_POST</span><span class="p">[</span><span class="s1">'username'</span><span class="p">]</span> <span class="p">)</span> <span class="p">)</span> <span class="k">echo</span> <span class="nx">esc_attr</span><span class="p">(</span> <span class="nv">$_POST</span><span class="p">[</span><span class="s1">'username'</span><span class="p">]</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">" /&gt;</span>
</span><span id="line-70"><span class="x">                    &lt;/p&gt;</span>
</span><span id="line-71"><span class="x">                    &lt;p class="form-row form-row-wide"&gt;</span>
</span><span id="line-72"><span class="x">                        &lt;label for="password"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Password'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x"> &lt;span class="required"&gt;*&lt;/span&gt;&lt;/label&gt;</span>
</span><span id="line-73"><span class="x">                        &lt;input class="input-text" type="password" name="password" id="password" /&gt;</span>
</span><span id="line-74"><span class="x">                    &lt;/p&gt;</span>
</span><span id="line-75">
</span><span id="line-76">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'woocommerce_login_form'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-77">
</span><span id="line-78"><span class="x">                    &lt;p class="form-row"&gt;</span>
</span><span id="line-79">                        <span class="cp">&lt;?php</span> <span class="nx">wp_nonce_field</span><span class="p">(</span> <span class="s1">'woocommerce-login'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-80"><span class="x">                        &lt;input type="submit" class="button" name="login" value="</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Login'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">" /&gt;</span>
</span><span id="line-81"><span class="x">                        &lt;label for="rememberme" class="inline"&gt;</span>
</span><span id="line-82"><span class="x">                            &lt;input name="rememberme" type="checkbox" id="rememberme" value="forever" /&gt; </span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Remember me'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-83"><span class="x">                        &lt;/label&gt;</span>
</span><span id="line-84"><span class="x">                    &lt;/p&gt;</span>
</span><span id="line-85"><span class="x">                    &lt;p class="lost_password"&gt;</span>
</span><span id="line-86"><span class="x">                        &lt;a href="</span><span class="cp">&lt;?php</span> <span class="k">echo</span> <span class="nx">esc_url</span><span class="p">(</span> <span class="nx">wc_lostpassword_url</span><span class="p">()</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Lost your password?'</span><span class="p">,</span> <span class="s1">'woocommerce'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">&lt;/a&gt;</span>
</span><span id="line-87"><span class="x">                    &lt;/p&gt;</span>
</span><span id="line-88">
</span><span id="line-89">                    <span class="cp">&lt;?php</span> <span class="nx">do_action</span><span class="p">(</span> <span class="s1">'woocommerce_login_form_end'</span> <span class="p">);</span> <span class="cp">?&gt;</span>
</span><span id="line-90">
</span><span id="line-91"><span class="x">                &lt;/form&gt;</span>
</span><span id="line-92">
</span><span id="line-93"><span class="x">            &lt;a href="</span><span class="cp">&lt;?php</span> <span class="k">echo</span> <span class="nx">get_permalink</span><span class="p">(</span><span class="nx">woocommerce_get_page_id</span><span class="p">(</span><span class="s1">'myaccount'</span><span class="p">))</span> <span class="o">.</span> <span class="s1">'?action=register'</span><span class="p">;</span> <span class="cp">?&gt;</span><span class="x">"&gt;</span><span class="cp">&lt;?php</span> <span class="nx">_e</span><span class="p">(</span> <span class="s1">'Register'</span> <span class="p">);</span> <span class="cp">?&gt;</span><span class="x">&lt;/a&gt;</span>
</span><span id="line-94">
</span><span id="line-95"><span class="x">            &lt;/div&gt; &lt;!-- end Login Section .col-sm-6 --&gt;</span>
</span><span id="line-96">
</span><span id="line-97">        <span class="cp">&lt;?php</span> <span class="k">endif</span><span class="p">;</span> <span class="cp">?&gt;</span>
</span><span id="line-98">
</span><span id="line-99"><span class="x">        &lt;/div&gt;</span>
</span><span id="line-100"><span class="x">      &lt;/div&gt;&lt;!-- end .col-xs-12 .col-sm-10 .col-sm-offset-1 --&gt;</span>
</span><span id="line-101"><span class="x">    &lt;/div&gt;&lt;!-- end .row --&gt;</span>
</span><span id="line-102">
</span><span id="line-103"><span class="cp">&lt;?php</span> <span class="k">endif</span><span class="p">;</span> <span class="cp">?&gt;</span></span></pre>