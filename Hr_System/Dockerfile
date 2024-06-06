# Use an official OpenJDK runtime as a parent image
# FROM openjdk:11-jre-slim

# Set the working directory in the container
# WORKDIR /app

# Copy the jar file from the target directory to the container
# COPY build/libs/Hr_System-0.0.1-SNAPSHOT.jar app.jar

# Make port 8080 available to the world outside this container
# EXPOSE 8080

# Run the jar file
# ENTRYPOINT ["java", "-jar", "app.jar"]

# ============================================================================

# 使用官方的 OpenJDK 作为基础镜像
FROM openjdk:11-jre-slim

# 设置工作目录
WORKDIR /app

# 将当前目录的内容复制到工作目录中
COPY . .

# 构建项目
RUN ./gradlew build

# 复制生成的 JAR 文件到工作目录中
COPY build/libs/Hr_System-0.0.1-SNAPSHOT.jar app.jar

# 暴露应用运行的端口
EXPOSE 8080

# 运行 Spring Boot 应用
ENTRYPOINT ["java", "-jar", "app.jar"]

# ============================================================================
# 使用官方的 OpenJDK 作为基础镜像
# FROM openjdk:11-jre-slim

# 设置工作目录
# WORKDIR /app

# 将 Hr_System 目录的内容复制到工作目录中
# COPY Hr_System .

# 构建项目
# RUN ./gradlew build

# 复制生成的 JAR 文件到工作目录中
# COPY Hr_System/build/libs/Hr_System-0.0.1-SNAPSHOT.jar app.jar

# 暴露应用运行的端口
# EXPOSE 8080

# 运行 Spring Boot 应用
# ENTRYPOINT ["java", "-jar", "app.jar"]