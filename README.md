# Test repo for [woorelease](https://github.com/woocommerce/woorelease)
Woorelease misses entries that were merged before **tag was created** - no but after the tagged commit/release.

1. Make a release `1.0.0` on commit _X_ without creating a tag, or delete the tag after the release.
2. Merge few PRs
3. (Re-)Create  the `1.0.0` on commit _X_
4. Try generating the changelog
```
woorelease cl:generate --product_version=1.0.1 https://github.com/woorelease-bugs/before-tag-time/tree/develop
```

And with https://github.com/woorelease-bugs/before-tag-time/releases/new?tag=1.0.1

## Prerequisites

We aim to support the latest two minor versions of WordPress, WooCommerce, and PHP. (L-2 policy)

-   WordPress 5.7+
-   WooCommerce 6.0+
-   PHP 7.3+

<p align="center">
	<br/><br/>
	Made with 💜 by <a href="https://woocommerce.com/">WooCommerce</a>.<br/>
	<a href="https://woocommerce.com/careers/">We're hiring</a>! Come work with us!
</p>
