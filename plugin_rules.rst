Plugin rules
============

 * The plugin system of Electrum is designed to allow the development
   of new features without increasing the core code of Electrum.

 * Electrum is written in pure python. if you want to add a feature
   that requires non-python libraries, then it must be submitted as a
   plugin. If the feature you want to add requires communication with
   a remote server (not an Electrum server), then it should be a
   plugin as well. If the feature you want to add introduces new
   dependencies in the code, then it should probably be a plugin.

 * We expect plugin developers to maintain their plugin code. However,
   once a plugin is merged in Electrum, we will have to maintain it
   too, because changes in the Electrum code often require updates in
   the plugin code. Therefore, plugins have to be easy to maintain. If
   we believe that a plugin will create too much maintenance work in
   the future, it will be rejected.

 * Plugins should be compatible with Electrum's conventions. If your
   plugin does not fit with Electrum's architecture, or if we believe
   that it will create too much maintenance work, it will not be
   accepted. In particular, do not duplicate existing Electrum code in
   your plugin.

 * We may decide to remove a plugin after it has been merged in
   Electrum. For this reason, a plugin must be easily removable,
   without putting at risk the user's bitcoins. If we feel that a
   plugin cannot be removed without threatening users who rely on it,
   we will not merge it.

