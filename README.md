# jyy
git help <command> # ��ʾcommand��help
git show # ��ʾĳ���ύ������ git show $id
git co -- <file> # �����������޸�
git co . # �����������޸�
git add <file> # �������ļ��޸��ύ�������ݴ���
git add . # �������޸Ĺ��Ĺ����ļ��ύ�ݴ���
git rm <file> # �Ӱ汾����ɾ���ļ�
git rm <file> --cached # �Ӱ汾����ɾ���ļ�������ɾ���ļ�
git reset <file> # ���ݴ����ָ��������ļ�
git reset -- . # ���ݴ����ָ��������ļ�
git reset --hard # �ָ����һ���ύ����״̬���������ϴ��ύ������б����޸�
git ci <file> git ci . git ci -a # ��git add, git rm��git ci�Ȳ������ϲ���һ����������������������������������������������������������������������������git ci -am "some comments"
git ci --amend # �޸����һ���ύ��¼
git revert <$id> # �ָ�ĳ���ύ��״̬���ָ���������Ҳ�������ύ����
git revert HEAD # �ָ����һ���ύ��״̬
�鿴�ļ�diff
git diff <file> # �Ƚϵ�ǰ�ļ����ݴ����ļ����� git diff
git diff <

id1><
id2> # �Ƚ������ύ֮��Ĳ���
git diff <branch1>..<branch2> # ��������֧֮��Ƚ�
git diff --staged # �Ƚ��ݴ����Ͱ汾�����
git diff --cached # �Ƚ��ݴ����Ͱ汾�����
git diff --stat # �����Ƚ�ͳ����Ϣ
�鿴�ύ��¼
git log git log <file> # �鿴���ļ�ÿ���ύ��¼
git log -p <file> # �鿴ÿ����ϸ�޸����ݵ�diff
git log -p -2 # �鿴���������ϸ�޸����ݵ�diff
git log --stat #�鿴�ύͳ����Ϣ
tig
Mac�Ͽ���ʹ��tig����diff��log��brew install tig
Git ���ط�֧����
�鿴���л���������ɾ����֧
git br -r # �鿴Զ�̷�֧
git br <new_branch> # �����µķ�֧
git br -v # �鿴������֧����ύ��Ϣ
git br --merged # �鿴�Ѿ����ϲ�����ǰ��֧�ķ�֧
git br --no-merged # �鿴��δ���ϲ�����ǰ��֧�ķ�֧
git co <branch> # �л���ĳ����֧
git co -b <new_branch> # �����µķ�֧�������л���ȥ
git co -b <new_branch> <branch> # ����branch�����µ�new_branch
git co $id # ��ĳ����ʷ�ύ��¼checkout���������޷�֧��Ϣ���л���������֧���Զ�ɾ��
git co $id -b <new_branch> # ��ĳ����ʷ�ύ��¼checkout������������һ����֧
git br -d <branch> # ɾ��ĳ����֧
git br -D <branch> # ǿ��ɾ��ĳ����֧ (δ���ϲ��ķ�֧��ɾ����ʱ����Ҫǿ��)
?��֧�ϲ���rebase
git merge <branch> # ��branch��֧�ϲ�����ǰ��֧
git merge origin/master --no-ff # ��ҪFast-Foward�ϲ���������������merge�ύ
git rebase master <branch> # ��master rebase��branch���൱�ڣ� git co <branch> && git rebase master && git co master && git merge <branch>