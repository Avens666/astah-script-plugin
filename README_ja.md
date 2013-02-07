Astah Script Plugin
=============================
![dialog image](https://github.com/ChangeVision/astah-script-plugin/raw/master/doc/screenshots/script_dialog_ja.png)

�o�[�W����
------------
1.0.0

�ΏۃG�f�B�V����
------------------
Astah Community, UML, and Professional 6.5.x �ȍ~
�T���v���X�N���v�g�̈ꕔ�́AAstah UML�AAstah Professional�݂̂ŗ��p�\�B
Astah: http://astah.change-vision.com/ja/

�T�v
------------
�X�N���v�g�����Astah�ɃA�N�Z�X�ł��܂��BECMAScript(JavaScript)�̕ҏW�Ǝ��s���\�ł��B

�C���X�g�[���̗���
------------
1. [Download](http://cdn.change-vision.com/plugins/astah_script_plugin-1.0.0.zip)���� zip�t�@�C�����_�E�����[�h���A�C�ӂ̃t�H���_�֓W�J���܂��B

    ��) Astah Professional, Windows: `$USER_HOME/.astah/professional/plugins/`,  `C:\Program Files\astah-professional\plugins\`
    Astah Professional, Mac OS X: `/Applications/astah professional/plguins/`
    
    ��) Astah Community, Windows: `$USER_HOME/.astah/community/plugins/`, `C:\Program Files\astah-community\plugins\`
    Astah Community, Mac OS X: `/Applications/astah community/plguins/`

2. Astah���N�����܂��B

3. �㕔���j���[[�c�[��]�z���� [�X�N���v�g]���ǉ�����Ă��܂��B

![menu image](https://github.com/ChangeVision/astah-script-plugin/raw/master/doc/screenshots/script_plugin_menu_ja.png)

�g����
------------

1. Astah���N�����A�X�N���v�g�����s�������v���W�F�N�g�t�@�C��(.asta)���J���܂��B
2. Astah�㕔���j���[[�c�[��]-[�X�N���v�g]��I������ƁA�V�K�X�N���v�g�_�C�A���O���J���܂��B
3. ��i�ɃX�N���v�g����͂��邩�A�܂��̓X�N���v�g�_�C�A���O�̃��j���[[�t�@�C��]-[�J��]��I�����A�\�ߗp�ӂ��Ă�����JavaScript�̃t�@�C�����J���܂��B  
   �T���v���X�N���v�g�͌�҂̕��@�ł��������������B
4. �X�N���v�g�_�C�A���O�̃��j���[[�A�N�V����]-[���s]��I�����܂��B(�V���[�g�J�b�g�L�[ [Ctrl+R]�ł����s�ł��܂�)
5. ���i�Ɍ��ʂ��\������܂��B
6. ��i�ɓ��͂����X�N���v�g�� [�t�@�C��]-[���O��t���ĕۑ�]�ŕۑ��ł��܂��B


�T���v���X�N���v�g
---------------------
`sample_scripts` �t�H���_�ɂ́A���v14�P��JavaScript�T���v���t�@�C�����i�[����Ă��܂��B

 * addSetterGetter.js
 * addStereotypeToSelectedModel.js
 * checkEdition.js
 * countClasses.js
 * createAndOpenDiagram.js
 * createEREntities.js
 * exportCsv.js
 * printClasses.js
 * printERIndex.js
 * printMindmapTopics.js
 * printPackageAndClassInfo.js
 * printPresentationProperties.js
 * searchAndEdit.js
 * useJavaGUI.js

��) JavaScript: `printClasses.js`
```javascript
importPackage(com.change_vision.jude.api.inf.model);
var classes = astah.findElements(IClass);
for(var i in classes) {
    println(classes[i].getName());
}
```
 * ��`�ς݂̕ϐ����g���܂��B
   * `projectAccessor`
     * It's an object of ProjectAccessor in Astah API.
     * `null` if Astah has no project.
   * `astah`
     * It's same as `projectAccessor`.
   * `astahWindow`
     * Astah���C���E�B���h�E�I�u�W�F�N�g
   * `scriptWindow`
     * It's the window object of the script plugin.
 * �X�N���v�g�� Astah API���g���܂��B
   * Astah API �T�v
     * <http://astah.change-vision.com/ja/astah-api.html>
   * Astah API ���p�K�C�h (Javadoc)
     * <http://members.change-vision.com/javadoc/astah-api/latest/api/en/doc/javadoc/index.html>
 * You are able to use the Java API in your script.

�r���h
------------
1. Astah Plug-in SDK���C���X�g�[�����܂��B - <http://astah.change-vision.com/ja/plugins.html>
2. `git clone git://github.com/ChangeVision/astah-script-plugin.git`
3. `cd script`
4. `astah-build`
5. `astah-launch`

 * Generating config to load classpath [for Eclipse](http://astah.net/tutorials/plug-ins/plugin_tutorial_en/html/helloworld.html#eclipse)

      * `astah-mvn eclipse:eclipse`

���̃X�N���v�g������g��
------------
OSGi JSR223�����̑��̃X�N���v�g������g�p�ł��܂��B

1. �g�p�������X�N���v�g����� jar�t�@�C�����_�E�����[�h���܂��B(��. groovy-all.jar, jruby-###.jar)
2. Astah plugins �t�H���_�� 1��jar�t�@�C�����R�s�[���܂��B(~/.astah/plugins)
3. Astah���N�����܂�

License
------------
Copyright 2012 Change Vision, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   <http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Third party software licenses
------------
 * RSyntaxTextArea is licensed under modified BSD License.  Please see the included license file.
 * AutoComplete is licensed under modified BSD License.  Please see the included license file.

