# basic

[Java Service Provider Interface ](https://itnext.io/java-service-provider-interface-understanding-it-via-code-30e1dd45a091)

SPI
META-INF/services
java.util.ServiceLoader

			ServiceLoader<IAccount> loader = ServiceLoader.load(IAccount.class);
			
			Iterator<IAccount> iterator = loader.iterator();
			
			List<AccountTO> accountList = new ArrayList<>();
			
			while(iterator.hasNext()) {
				IAccount next = iterator.next();
				AccountTO acc = new AccountTO();
				acc.setAccountId(next.getAccountId());
				acc.setAccountType(next.getAccountType());
				accountList.add(acc);
			}
			