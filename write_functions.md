writing\_functions
================
JiyueQin
October 25, 2018

# small functions

``` r
x = rnorm(25, 5, 3)
(x - mean(x)) / sd(x)
```

    ##  [1] -0.33628538 -1.61851716 -0.14614466  1.25304763  1.22785778
    ##  [6]  1.83067059 -1.71421176 -0.07199048  0.18722740  0.47513108
    ## [11] -0.38626369 -1.26128802  0.79408272  1.26571408  0.98854244
    ## [16] -0.02530214 -0.02936677 -2.18773372  0.04768375 -0.72481619
    ## [21] -0.14534611 -0.45251215  1.05372480  0.06098339 -0.08488743

``` r
z_scores = function(x) {
  
  (x - mean(x)) / sd(x)
  
}

y = runif(100)
z_scores(y)
```

    ##   [1] -1.1726139 -1.0584411  1.7421245  0.3061265 -1.0916593  0.3920729
    ##   [7] -1.0390445 -0.4212799 -1.0780966  1.9110762 -0.5252061 -0.8505527
    ##  [13] -0.1788556  1.9297200  0.7710061 -1.2397416  1.0897055 -0.9931752
    ##  [19] -0.1762793  0.9680109  0.7541880  0.3008474  0.3673135  1.4078944
    ##  [25]  0.6006857 -0.7181365 -1.0342064  0.6618617 -0.9602380 -1.2461978
    ##  [31] -1.0114169 -1.4022801 -0.8514906  1.6561015  1.1533936 -0.9006524
    ##  [37] -0.6473273  1.7176826  1.0374717  1.3846478 -0.8105969 -0.8168692
    ##  [43]  1.8703331  1.6878559 -1.1710085  1.6809004 -0.4332652 -0.4837414
    ##  [49]  0.8353456 -1.0208557 -0.8766111 -0.1768454 -0.7921870 -1.0403642
    ##  [55]  0.4622807  0.1009633  1.7411115  0.6237183  1.3665402 -0.3532135
    ##  [61] -0.9465585 -0.2038756  0.5690358  0.1587972  1.2855842 -1.1021338
    ##  [67]  1.4605701 -1.3681267 -1.1570619  0.5499772  0.6461155 -0.4508029
    ##  [73]  0.3492076 -0.8587805 -0.7845654 -1.0467198 -0.1491884  0.9701468
    ##  [79] -0.5056232  1.5856946  0.5206207  1.5178170  0.2122742 -0.2221836
    ##  [85]  0.4223807  1.7193448  0.1912188 -1.3014605 -0.5960615 -0.1838181
    ##  [91] -0.4149746 -0.1993025  0.6255821 -0.2119015 -1.3525816 -1.1190496
    ##  [97] -0.7169245 -0.9977338 -1.0976841  0.2542152

``` r
z_scores(x = y)
```

    ##   [1] -1.1726139 -1.0584411  1.7421245  0.3061265 -1.0916593  0.3920729
    ##   [7] -1.0390445 -0.4212799 -1.0780966  1.9110762 -0.5252061 -0.8505527
    ##  [13] -0.1788556  1.9297200  0.7710061 -1.2397416  1.0897055 -0.9931752
    ##  [19] -0.1762793  0.9680109  0.7541880  0.3008474  0.3673135  1.4078944
    ##  [25]  0.6006857 -0.7181365 -1.0342064  0.6618617 -0.9602380 -1.2461978
    ##  [31] -1.0114169 -1.4022801 -0.8514906  1.6561015  1.1533936 -0.9006524
    ##  [37] -0.6473273  1.7176826  1.0374717  1.3846478 -0.8105969 -0.8168692
    ##  [43]  1.8703331  1.6878559 -1.1710085  1.6809004 -0.4332652 -0.4837414
    ##  [49]  0.8353456 -1.0208557 -0.8766111 -0.1768454 -0.7921870 -1.0403642
    ##  [55]  0.4622807  0.1009633  1.7411115  0.6237183  1.3665402 -0.3532135
    ##  [61] -0.9465585 -0.2038756  0.5690358  0.1587972  1.2855842 -1.1021338
    ##  [67]  1.4605701 -1.3681267 -1.1570619  0.5499772  0.6461155 -0.4508029
    ##  [73]  0.3492076 -0.8587805 -0.7845654 -1.0467198 -0.1491884  0.9701468
    ##  [79] -0.5056232  1.5856946  0.5206207  1.5178170  0.2122742 -0.2221836
    ##  [85]  0.4223807  1.7193448  0.1912188 -1.3014605 -0.5960615 -0.1838181
    ##  [91] -0.4149746 -0.1993025  0.6255821 -0.2119015 -1.3525816 -1.1190496
    ##  [97] -0.7169245 -0.9977338 -1.0976841  0.2542152

``` r
z_scores(3)
```

    ## [1] NA

``` r
kz_scores("my name is jeff")
```

    ## Error in kz_scores("my name is jeff"): could not find function "kz_scores"

``` r
z_scores(iris)
```

    ## Warning in mean.default(x): argument is not numeric or logical: returning
    ## NA

    ## Warning in Ops.factor(left, right): '-' not meaningful for factors

    ## Error in is.data.frame(x): (list) object cannot be coerced to type 'double'

``` r
z_scores(sample(c(TRUE, FALSE), 25, replace = TRUE))
```

    ##  [1] -1.0198039  0.9413574 -1.0198039  0.9413574  0.9413574 -1.0198039
    ##  [7]  0.9413574 -1.0198039 -1.0198039  0.9413574 -1.0198039 -1.0198039
    ## [13] -1.0198039  0.9413574  0.9413574 -1.0198039  0.9413574  0.9413574
    ## [19]  0.9413574 -1.0198039  0.9413574  0.9413574 -1.0198039 -1.0198039
    ## [25]  0.9413574

# having checks

``` r
z_scores = function(x) {
  
  if (!is.numeric(x)) {
    stop("Argument x should be numeric")
  } else if (length(x) == 1) {
    stop("Z scores cannot be computed for length 1 vectors")
  }
  
  z = mean(x) / sd(x)
  
  z
}
```

# having multiple outputs

``` r
mean_and_sd = function(x) {
  
  if (!is.numeric(x)) {
    stop("Argument x should be numeric")
  } else if (length(x) == 1) {
    stop("Cannot be computed for length 1 vectors")
  }
  
  mean_x = mean(x)
  sd_x = sd(x)
  c(mean_x, sd_x)
  
  list(mean = mean_x, 
       sd = sd_x)
}
mean_and_sd(y)
```

    ## $mean
    ## [1] 0.4229613
    ## 
    ## $sd
    ## [1] 0.2856845

``` r
# more readable
mean_and_sd = function(x) {
  
  if (!is.numeric(x)) {
    stop("Argument x should be numeric")
  } else if (length(x) == 1) {
    stop("Cannot be computed for length 1 vectors")
  }
 
  tibble(mean_x = mean(x),
         sd_x = sd(x))
}

mean_and_sd(y)
```

    ## # A tibble: 1 x 2
    ##   mean_x  sd_x
    ##    <dbl> <dbl>
    ## 1  0.423 0.286

``` r
mean_and_sd = function(x) {
  
  if (!is.numeric(x)) {
    stop("Argument x should be numeric")
  } else if (length(x) == 1) {
    stop("Cannot be computed for length 1 vectors")
  }
  
  mean_x = mean(x)
  sd_x = sd(x)
  
  list(mean = mean_x, 
       sd = sd_x)
}
```

## multiple inputs

``` r
sim_data = tibble(
  x = rnorm(30, mean = 1, sd = 1),
  y = 2 + 3 * x + rnorm(30, 0, 1)
)

ls_fit = lm(y ~ x, data = sim_data)
  
beta0_hat = coef(ls_fit)[1]
beta1_hat = coef(ls_fit)[2]
```

write the function that simulates the data

``` r
sim_regression = function(n, beta0 = 2, beta1 = 3) {
  
  sim_data = tibble(
    x = rnorm(n, mean = 1, sd = 1),
    y = beta0 + beta1 * x + rnorm(n, 0, 1)
  )
  
  ls_fit = lm(y ~ x, data = sim_data)
  
  tibble(
    beta0_hat = coef(ls_fit)[1],
    beta1_hat = coef(ls_fit)[2]
  )
}

sim_regression(n = 3000, 0 , -1)
```

    ## # A tibble: 1 x 2
    ##   beta0_hat beta1_hat
    ##       <dbl>     <dbl>
    ## 1   -0.0219     -1.01

``` r
sim_regression(beta0 = 0, beta1 = -1, n = 3000)
```

    ## # A tibble: 1 x 2
    ##   beta0_hat beta1_hat
    ##       <dbl>     <dbl>
    ## 1    0.0207     -1.01

# revisit amazon review

``` r
read_page_reviews <- function(url) {
  
  h = read_html(url)
  
  review_titles = h %>%
    html_nodes("#cm_cr-review_list .review-title") %>%
    html_text()
  
  review_stars = h %>%
    html_nodes("#cm_cr-review_list .review-rating") %>%
    html_text() %>%
    str_extract("\\d") %>%
    as.numeric()
  
  review_text = h %>%
    html_nodes(".review-data:nth-child(4)") %>%
    html_text()
  
  tibble(
    title = review_titles,
    stars = review_stars,
    text = review_text
  )
}
url_base = "https://www.amazon.com/product-reviews/B00005JNBQ/ref=cm_cr_arp_d_viewopt_rvwer?ie=UTF8&reviewerType=avp_only_reviews&sortBy=recent&pageNumber="
urls = str_c(url_base, 1:5)

dynamite_reviews = bind_rows(
  read_page_reviews(urls[1]),
  read_page_reviews(urls[2]),
  read_page_reviews(urls[3]),
  read_page_reviews(urls[4]),
  read_page_reviews(urls[5])
)

dynamite_reviews
```

    ## # A tibble: 50 x 3
    ##    title                     stars text                                   
    ##    <chr>                     <dbl> <chr>                                  
    ##  1 "Great \"Odd Ball\" movi~     5 The dance scene was worth the time spe~
    ##  2 Nostalgic Stupidity           4 This movie is dumb. I won't lie and sa~
    ##  3 Happy                         5 Don't know why I lov this movie but ido
    ##  4 Go watch THE ROCK or dum~     2 This movie is horrible. How do so many~
    ##  5 My mom loves it               5 Got this for my mom for mother's day, ~
    ##  6 Nothing Quite Like It.        5 So much fun watching these listless pe~
    ##  7 Has pretty sweet bow ski~     5 Well, things are getting pretty seriou~
    ##  8 Great                         5 Great                                  
    ##  9 Fast delivery                 5 Bought as gift                         
    ## 10 Lol                           5 Funny                                  
    ## # ... with 40 more rows
