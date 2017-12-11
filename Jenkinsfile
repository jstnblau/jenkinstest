properties([
	parameters([
		string(defaultValue: '', description: 'Full name: <first_name> <last name>', name: 'full_name'),
		string(defaultValue: '', description: 'LDAP2 user ID', name: 'user_id'),
		string(defaultValue: '', description: 'Email address', name: 'email'),
		booleanParam(defaultValue: '', description: 'I read Onboarding Document: https://wiki.mlbam.com/display/AWS/Bamazon+Onboarding', name: 'onboarding'),
		booleanParam(defaultValue: '', description: 'I took bamazon quiz: https://quiz.us-east-1.bamgrid.net/', name: 'quiz'),
		string(defaultValue: '', description: 'Password hash', name: 'hash'),
		string(defaultValue: '', description: 'SSH public key', name: 'pub_key')
		choice(choices: 'activation\nadtech\napiservices\nbbenter\nbcastinfra\nbdata\nbta\ncd\ncde\ncdo\ncedcons\ncms\ncoreeng\ncoreengops\ncoremedia\ndba\ndbapci\neis\nengage\nentmedia\nepg\nepgsf\nfed\nfeddigitalprimates\nfedvector\ninfosec\nmdrm\nmmdev\nmobile\nnetadmins\npivotalmmdevnhl\npivotalskynet\nproductops\nqa\nreplay\nsearch\nsdata\nsentv\nskynet\nstrm\nsysops\nsystems\ntavantcms\ntavantskynetnhl\nticketing\nuserservices', description: '', name: 'groups')
		])])


def puppetModuleBuilds = fileLoader.fromGit(
  'puppet-modules/createusers.groovy',
  'https://github.mlbam.net/cec-groovy/libjenkins',
  'master',
  'github-user'
)

puppetModuleBuilds.createec2user()