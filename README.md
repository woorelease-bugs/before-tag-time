# Test repo for [woorelease](https://github.com/woocommerce/woorelease)
Woorelease misses entries that were merged before **tag was created** - no but after the tagged commit/release.

1. Make a release `1.0.0` on commit _X_ without creating a tag, or delete the tag after the release.
2. Merge few PRs
3. (Re-)Create  the `1.0.0` on commit _X_

   ![image](https://user-images.githubusercontent.com/17435/174164201-5aa373ee-8919-427d-ac95-332cf31b2283.png)

4. Try generating the changelog
	```
	woorelease cl:generate --product_version=1.0.1 https://github.com/woorelease-bugs/before-tag-time/tree/develop
	```
	```
	WR [23:10:10] [NOTICE] Retrieving merged PR's since version 1.0.0 released on 2022-06-16 23:09:19
	WR [23:10:11] [WARNING] Could not find any data for generated changelog.
	WR [23:10:11] [WARNING] Could not find any current changelog entries in changelog.txt.
	WR [23:10:15] [ERROR] No valid changelog entries found in 
	```


5. And with https://github.com/woorelease-bugs/before-tag-time/releases/new?tag=1.0.1 "Generate release notes"
	```
	## What's Changed
	### New Features 🎉
	* Add a workflow to attach label based on PR branchname by @tomalec in https://github.com/woorelease-bugs/before-tag-time/pull/1
	* Add release.yml by @tomalec in https://github.com/woorelease-bugs/before-tag-time/pull/2
	```

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
